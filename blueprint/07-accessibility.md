# 07 — Accessibility

**Target: WCAG 2.1 AA baseline.**

Not optional. Legally expected. Also makes the site work better for everyone.

---

## Images (LOCKED)

- Every `<img>` has an `alt` attribute.
- Decorative images: `alt=""` (empty but present).
- Meaningful images: descriptive alt text. Example: `alt="Custom timber-frame home built in Garden Valley"`.
- The hero image `alt` describes the landscape, not the company.

---

## Buttons & Links (LOCKED)

- Tap-to-call phone: `<a href="tel:+12082593378" aria-label="Call Jackson and Grear at 208-259-3378">208-259-3378</a>`
- Tap-to-email (when live): `<a href="mailto:[email]" aria-label="Email Jackson and Grear">[email]</a>`
- Icon-only buttons (like hamburger menu): must have `aria-label`.
- Every button has visible text OR an `aria-label`.

---

## Keyboard Navigation (LOCKED)

- All interactive elements reachable via Tab key in logical order.
- Focus states visible — 2px outline in `--color-sage` with 2px offset (see `03-design.md`).
- Hamburger menu opens/closes with Enter or Space.
- Skip-to-content link at the top of every page (hidden until keyboard-focused).

---

## Color Contrast (LOCKED)

- Body text (`--color-ink` on `--color-base`): must meet 4.5:1 contrast ratio.
- Large text (18pt+ or 14pt bold): must meet 3:1.
- Button text (`--color-base` on `--color-accent`): must meet 4.5:1.
- Build chat verifies with a contrast checker (e.g. WebAIM contrast checker) before Phase 2 sign-off.

**If any pair fails:** adjust the token value in `03-design.md`, document in `DECISIONS.md`, and re-verify.

---

## Semantic HTML (LOCKED)

- Use `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>` — not `<div>` for everything.
- Headings in order: one `<h1>` per page, then `<h2>`, `<h3>`, no skipping levels.
- `<main>` wraps the primary content of every page.

---

## Motion (LOCKED)

- Respect `prefers-reduced-motion: reduce` — disable all transitions and transforms.
- No auto-playing anything (no carousels, no videos, no animated backgrounds).

---

## Forms (N/A — no forms in scope)

If a contact form is ever added later, it must include:
- Associated `<label>` for every input.
- Clear error messages tied to inputs via `aria-describedby`.
- No placeholder-as-label.

---

## Language (LOCKED)

- `<html lang="en">` on every page.

---

**Status: LOCKED.**
