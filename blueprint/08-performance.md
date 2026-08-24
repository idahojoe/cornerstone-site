# 08 — Performance & Browser Support

**Critical context:** Most visitors are on mobile, on rural Idaho cell service. Bloat kills usability.

---

## Performance Budget (LOCKED)

| Resource | Max size |
|---|---|
| Hero image (compressed) | 500 KB |
| Project gallery photo | 300 KB each |
| Total page weight (any single page) | 2 MB |
| CSS file | 50 KB |
| JS file | 20 KB (or none) |
| Web fonts (total) | 200 KB |

**If a page exceeds 2 MB total:** stop, compress images further, remove non-essential assets.

---

## Image Optimization (LOCKED)

- Hero and project photos delivered as `.jpg` at 80% quality.
- Logo delivered as `.png` (transparent) or `.svg` if provided.
- Favicon as `.png` at 32×32.
- Consider `.webp` versions with `.jpg` fallback if page weight is close to budget.
- All images use `loading="lazy"` except the hero (which loads eagerly).

---

## Fonts (LOCKED)

- Google Fonts loaded via `<link>` with `display=swap` for fast text render.
- Only load weights actually used:
  - Fraunces: 500, 600
  - Inter: 400, 500
  - Space Mono (or JetBrains Mono): 400
- No local font hosting unless Google Fonts is blocked.

---

## CSS & JS (LOCKED)

- One CSS file, minified for production if needed (owner can skip minification for readability if page weight is fine).
- JS only if strictly necessary — hamburger menu toggle, that's it. If it can be done with CSS alone (e.g. `:target` or `<details>`), prefer CSS.
- No jQuery. No frameworks. No polyfills.

---

## Browser Support (LOCKED)

- **Supported:** Latest 2 versions of Chrome, Safari, Firefox, Edge on desktop and mobile.
- **Not supported:** IE 11, legacy Edge, browsers older than 2 years.
- **Rationale:** Modern CSS Grid, custom properties, and `object-fit` all require modern browsers. Trying to support older browsers adds bloat and complexity for near-zero real-world users.

---

## Loading Priorities (LOCKED)

- **Critical:** HTML, CSS, hero image.
- **Deferred:** JS (if any), non-hero images (`loading="lazy"`).
- **Fonts:** Loaded async via Google Fonts `display=swap`.

---

## Print Styles (LOCKED)

Small `@media print` block in CSS:
- Hide nav and footer.
- Hide buttons.
- Keep phone number and email visible and readable.
- Body text in black on white.
- Contact page prints clean as a one-page reference.

---

**Status: LOCKED.**
