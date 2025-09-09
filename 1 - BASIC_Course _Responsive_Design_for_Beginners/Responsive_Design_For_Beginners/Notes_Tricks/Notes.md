# 🌐 Project Setup

## STEP 1: CSS Location

- Load stylesheet from **dist** folder:
  ```html
  <link rel="stylesheet" href="/dist/style.css" />
  ```

Reason: style.css is generated from SASS (style.scss).

## STEP 2: JS Location

Load JavaScript file from app/js:

<script src="/app/js/script.js"></script>

## STEP 3: Project Folder Structure

app/
├── scss/ # SASS/SCSS files
│ └── style.scss
└── js/ # JavaScript files
└── script.js
dist/
└── style.css # Compiled CSS
index.html

## STEP 4: SCSS File

Create style.scss inside app/scss/.

Compile it into dist/style.css.

🎨 Best Practice: Colors

Always use HSL format:
// Example
$primary-color: hsl(200, 100%, 50%);
body {
background-color: $primary-color;
}

---

# 🎨 Compile SASS → CSS in VS Code

---

## ⚡ Required Extensions

1. **Live Sass Compiler** (by Glenn Marks)
2. **Live Server** (by Ritwick Dey)

---

## 🛠️ Steps to Compile SCSS into CSS

### STEP 1: Install Extensions

- Install **Live Sass Compiler** (Glenn Marks).
- Install **Live Server** (Ritwick Dey).

---

### STEP 2: Update Settings

1. Open **Command Palette** → `Ctrl+Shift+P` (Win/Linux) or `Cmd+Shift+P` (Mac).
2. Type: `Preferences: Open User Settings (JSON)`.
3. Add the following config:

```json
"liveSassCompile.settings.formats": [
  {
    "format": "expanded",
    "extensionName": ".css",
    "savePath": "/dist",
    "savePathReplacementPairs": null
  }
]


Run Compiler

Open your .scss file.

Click "Watch Sass" (from VS Code bottom bar).

Every time you save, SCSS compiles automatically → dist/style.css.



Notes & Best Practices

Browsers only understand CSS, not SCSS → compilation is always required.

Keep source files (SCSS) and output (CSS) in separate folders (app/ vs dist/).

You can change "savePath" to any folder you like (/css, /public/styles, etc.).

Use HSL colors in SCSS for readability & flexibility.
```
