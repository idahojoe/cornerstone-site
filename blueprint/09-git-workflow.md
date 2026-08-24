# 09 — Git Workflow, Deploy, Backup

---

## Branch Strategy (LOCKED)

- **`main` branch only.**
- No feature branches, no dev branches. Overkill for a 5-page site with a single owner.
- Every push to `main` auto-deploys to GitHub Pages.

---

## Commit Message Format (LOCKED)

Format: `phase X: short description`

Examples:
- `phase 1: scaffold repo structure and empty files`
- `phase 2: global styles, nav, footer, buttons`
- `phase 3: home page hero and layout`
- `photos: swap hero-home.jpg for owner photo`
- `content: update phone number on contact page`

**Rules:**
- Lowercase, imperative mood ("add" not "added").
- Under 72 chars.
- If change spans multiple phases or scope, split into multiple commits.

---

## Deploy (LOCKED)

- **Trigger:** Push to `main`.
- **Platform:** GitHub Pages.
- **Config:** Deploy from `main` branch, root folder (`/`).
- **Domain:** Free `*.github.io` at launch. Custom `.com` added via `CNAME` file at repo root when owner buys domain.
- **Cache:** GitHub Pages caches for ~10 minutes. Owner may need to hard-refresh (Cmd+Shift+R) to see updates immediately.

---

## Backup Plan (LOCKED)

- **Primary:** GitHub repo (cloud, private).
- **Secondary:** Owner downloads a zip of the repo once a month. Stores on personal computer or Google Drive.
- **How:** GitHub → repo → Code → Download ZIP.
- **Why:** If GitHub account is ever locked, disabled, or lost, owner has a full copy.

---

## Repo Access (LOCKED)

- **Visibility:** Private.
- **Contributors:** Owner (Joseph Grear) only at launch. Add Jeremiah Jackson if he wants access.
- **License file:** Not required (private repo).

---

## Post-Launch Update Flow (documented in `README.md`)

**Change text on a page:**
1. Open the `.html` file in GitHub web editor (or locally).
2. Edit the text.
3. Commit → push. Live in ~30 seconds.

**Swap a photo:**
1. Delete old photo from `/images/` folder in GitHub.
2. Upload new photo with the **same filename**.
3. Commit. Live in ~30 seconds.

**Add a project photo:**
1. Compress photo to under 300 KB.
2. Rename to next sequential number (`project-01.jpg`, `project-02.jpg`, etc.).
3. Upload to `/images/projects/`.
4. Add `<img>` tag to `projects.html` (see gallery pattern).
5. Commit → push.

**Update phone or email:**
1. Search across `.html` files for the old value.
2. Replace everywhere.
3. Commit → push.

---

**Status: LOCKED.**
