# 05 — Photos

---

## Workflow (LOCKED)

- Photos are named by purpose. Never by hash, date, or random string.
- To swap a photo: **replace the file with the same filename**, commit, push. Done.
- HTML never needs editing to swap a photo.
- Build chat must never hardcode image references in a way that breaks on filename-based replacement.

**Naming conventions:**
- Hero images: `hero-<page>.jpg` (e.g. `hero-home.jpg`)
- Project gallery: `project-01.jpg`, `project-02.jpg`, etc. (zero-padded, sequential)
- Logo: `logo.png`
- Favicon: `favicon.png`

---

## Dimensions (LOCKED)

| Type | Dimensions | Aspect ratio | Max file size |
|---|---|---|---|
| Hero | 1920 × 1080 | 16:9 | 500 KB (compressed) |
| Project gallery | 1200 × 900 | 4:3 | 300 KB |
| Logo | Provided as-is | — | 100 KB |
| Favicon | 32 × 32 | 1:1 | 10 KB |

**Auto-cropping:** CSS uses `object-fit: cover` on all image containers, so photos at the wrong ratio still display cleanly. Owner should not need to resize before uploading, but should compress large files.

**Owner tools for compression (free):**
- [squoosh.app](https://squoosh.app) — drag-and-drop, browser-based
- macOS Preview → Export → adjust quality slider

---

## Missing Photo Handling (LOCKED)

If a photo file is missing:
- Display a neutral placeholder box using `--color-base` background with a 1px `--color-secondary` border.
- No broken-image icon.
- No console errors on missing project photos (they're expected to be absent early).

---

## Hero Image Source (LOCKED)

- **Source:** [Unsplash](https://unsplash.com) — free for commercial use, no attribution required.
- **Content:** Idaho / mountain-West landscape. Sawtooths, Ponderosa forest, Boise County terrain, or similar.
- **Selection:** Build chat picks one Unsplash photo, downloads, compresses to under 500 KB, saves as `hero-home.jpg`.
- **Replacement:** Owner swaps with own photo when available. Same filename.

---

**Status: LOCKED.**
