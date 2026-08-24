# 04 — File & Folder Structure

---

## Repo Layout (LOCKED)

```
cornerstone-site/
├── index.html
├── services.html
├── projects.html
├── about.html
├── contact.html
├── 404.html
├── robots.txt
├── sitemap.xml
├── .gitignore
├── css/
│   └── style.css
├── js/
│   └── script.js
├── images/
│   ├── hero/
│   │   └── hero-home.jpg
│   ├── projects/
│   │   └── (empty until owner adds photos)
│   └── logo/
│       └── (empty until owner provides logo + favicon)
├── /blueprint/
│   └── (this planning folder — kept in repo for reference)
├── README.md
├── STATUS.md
├── DECISIONS.md
└── CHANGELOG.md
```

**Rules:**
- One CSS file (`css/style.css`). One JS file (`js/script.js`), only if needed.
- Photos live in `/images/` subfolders by purpose.
- All tracking files live at repo root.
- Blueprint folder stays in the repo so future chats / contributors can reference it.

---

## `.gitignore` (LOCKED)

Standard file. Blocks OS junk, editor configs, temp files.

```
# OS
.DS_Store
Thumbs.db
desktop.ini

# Editors
.vscode/
.idea/
*.swp
*.swo
*~

# Logs
*.log

# Env / secrets (defensive — no secrets in this project, but standard)
.env
.env.local

# Node (defensive — no node in this project, but standard)
node_modules/

# Build output (defensive — no build in this project, but standard)
dist/
build/
```

---

**Status: LOCKED.**
