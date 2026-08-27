# 03 — Design System

**This file bakes in Anthropic's `frontend-design` skill principles. The build chat must read and follow the skill before executing Phase 2 (Global Styles).**

Skill location: `/mnt/skills/public/frontend-design/SKILL.md`

---

## Design Thesis

**Subject:** A working construction outfit in rural Boise County, Idaho. Serves Lowman, Garden Valley, Stanley. Small-town values. Real trades work — concrete, framing, roofing, siding, remodels.

**Audience:** Rural homeowners, mostly on mobile, mostly on rural cell service. They want to know: are these guys real, can they do the job, how do I call them.

**Page's single job:** Convince a visitor in 10 seconds that these are competent local builders, and get them to call.

**Aesthetic direction:** Grounded in the actual materials of the trade and the landscape — weathered wood, mountain granite, sawdust, iron rust, pine shadow. Not templated "warm cream + terracotta serif" (AI default). Not corporate. Not rustic-cute. Working, honest, well-made.

**One aesthetic risk:** Nav uses an industrial-grade sans in ALL CAPS with wide tracked letter spacing — reads like it's stamped on job-site equipment. Everything else stays quiet and disciplined.

---

## Color Palette (LOCKED)

Named tokens. Build chat uses these exact values via CSS custom properties.

| Token | Hex | Use |
|---|---|---|
| `--color-base` | `#F2EDE0` | Page background — warm off-white, sawdust cream (warmer than #F4F1EA to avoid the AI-default) |
| `--color-ink` | `#1C2620` | Primary text — deep pine-shadow near-black-green |
| `--color-accent` | `#8B3A1F` | Weathered iron rust — accent, buttons, links |
| `--color-accent-dark` | `#6B2A15` | Button hover state |
| `--color-secondary` | `#6E6A5F` | Muted concrete gray — secondary text, borders |
| `--color-sage` | `#8A8F72` | Muted sagebrush green — subtle highlights, section dividers |

**Rules:**
- Base and ink together form the primary contrast. Verify contrast ratio meets WCAG AA (4.5:1 for body, 3:1 for large text).
- Accent (rust) is the boldness — use with restraint. Buttons, key links, signature moments.
- Sage is a supporting note only. Not a headline color.
- No gradients. No shadows deeper than a subtle 1px hairline where needed.

---

## Typography (LOCKED)

Google Fonts, loaded via `<link>` in `<head>`.

| Role | Family | Notes |
|---|---|---|
| Display (headlines) | **Libre Caslon Text** | Classical serif with warmth and quiet character — reads as an established, well-set page rather than a template. |
| Body | **Inter** | Clean, quiet, gets out of the way |
| Utility (nav, labels, captions) | **JetBrains Mono** or **Space Mono** | Monospace for nav caps and small utility text — the "stamped on equipment" signature |

**Type scale (spacious layout):**
- H1 (hero): 3.5rem desktop / 2.25rem mobile, Libre Caslon Text, weight 700
- H2 (section): 2.25rem desktop / 1.75rem mobile, Libre Caslon Text, weight 400
- H3: 1.5rem, Libre Caslon Text, weight 400
- Body: 1.125rem, Inter, weight 400, line-height 1.65
- Nav links: 0.75rem, Space Mono, uppercase, letter-spacing 0.15em
- Buttons: 1rem, Inter, weight 500, uppercase, letter-spacing 0.05em
- Footer / small: 0.875rem, Inter, weight 400

**Rules:**
- Do not swap font families. If a Google Fonts request fails, use `serif` / `sans-serif` / `monospace` system fallbacks — never substitute a different Google font.
- Libre Caslon Text is used sparingly and with restraint. Never for body text.

---

## Layout Principles (LOCKED)

- **Spacious.** Generous whitespace between sections.
- **Mobile-first.** Design mobile, scale up to desktop.
- **Max content width:** 1200px, centered.
- **Section vertical padding:** 6rem desktop / 3rem mobile.
- **Grid:** CSS Grid for layout. Flexbox for components.
- **Breakpoints:** 640px (small), 1024px (medium), 1280px (large). Mobile is default.

---

## Navigation Bar (LOCKED)

- **Top-left:** Company name in Libre Caslon Text (or logo image when provided).
- **Top-right (desktop):** `HOME` `SERVICES` `PROJECTS` `ABOUT` `CONTACT` — Space Mono, uppercase, wide letter-spacing.
- **Mobile:** Hamburger menu icon. Opens full-screen overlay with same links stacked.
- **Sticky:** Stays visible on scroll. Slight background blur or opacity to keep content readable underneath.
- **Active page:** Underlined with a 2px rust accent bar under the current page's nav link.

---

## Footer (LOCKED)

Three columns on desktop, stacked on mobile.

- **Left column:** Company name (Libre Caslon Text) + tagline: *Small-town values. Solid construction.*
- **Middle column:** Phone (tap-to-call), email (once available, tap-to-email), service area line.
- **Right column:** Quick links (same as nav).
- **Bottom line, centered, small type:** `© 2026 Jackson & Grear Cornerstone Construction. All rights reserved.`
- **Background:** `--color-ink` (deep pine-shadow). Text in `--color-base` (sawdust cream). Rust accent for links.

---

## Buttons (LOCKED)

- **Default:** Solid `--color-accent` (rust) background, `--color-base` (cream) text.
- **Text:** Inter, weight 500, uppercase, letter-spacing 0.05em.
- **Padding:** 0.875rem 1.75rem.
- **Border-radius:** 2px. Nearly square — reads like stamped metal, not soft/friendly.
- **Hover:** Background darkens to `--color-accent-dark`.
- **Focus:** Visible 2px outline in `--color-sage` with 2px offset. Keyboard-visible.
- **Active/pressed:** Slight scale down (transform: scale(0.98)).

**"Call for an estimate" button placement (from `02-pages-content.md`):**
- Home: in hero area
- Services: bottom of page
- Projects: bottom of page
- About: bottom of page
- Contact: prominent, near top

---

## Hero Section (LOCKED)

- **Background:** Full-width Idaho landscape photo from Unsplash (see `05-photos.md` for specs).
- **Overlay:** Semi-transparent `--color-ink` at ~35% opacity, so text is readable over any photo.
- **Content, centered:**
  - Company name in Libre Caslon Text, weight 700, in `--color-base`.
  - Tagline below in Inter, weight 400, in `--color-base` at 90% opacity.
  - Phone number as a large tap-to-call link.
  - "Call for an estimate" button.
- **Height:** 85vh on desktop, 70vh on mobile. Big, but not full-screen — visitor can see there's more below.

---

## Signature Element (LOCKED — the one memorable thing)

**Section dividers:** Instead of a plain line between sections, use a horizontal SVG element that reads as a subtle rust-textured mark — think a weathered pinstripe or a faint hairline stamped in `--color-accent`. Used once per section transition on Home and Services. Not decoration — a mark that says "this is a working outfit, not a corporate template."

**Restraint elsewhere:** Everything else stays quiet. No other decorative flourishes. No animated backgrounds. No parallax. No scroll effects beyond the sticky nav.

---

## Logo Handling (LOCKED)

- **Before owner provides logo:** Text logo — "Jackson & Grear" in Libre Caslon Text weight 700, "CORNERSTONE CONSTRUCTION" in Space Mono uppercase below at smaller size. This is the interim mark.
- **After owner provides logo:** Owner drops `logo.png` into `/images/logo/`. Build chat swaps text mark for image with minimal HTML/CSS change.
- **Favicon:** Skip until logo exists. Then drop 32x32 `favicon.png` into `/images/logo/`.

---

## Motion (LOCKED — restrained)

- **Nav:** Fade in on scroll. That's it.
- **Buttons:** Subtle hover color transition (150ms ease).
- **Hero:** No animation. Static.
- **Reduce motion:** Respect `prefers-reduced-motion: reduce` — disable all transitions and transforms.

---

## What NOT to do (from `frontend-design` skill)

- **Do not** default to warm cream + serif + terracotta accent (AI cliché #1).
- **Do not** use near-black background with acid-green or vermilion accent (AI cliché #2).
- **Do not** use broadsheet-style hairline rules with zero border-radius and dense columns (AI cliché #3).
- **Do not** add numbered markers (01 / 02 / 03) unless content is actually a sequence.
- **Do not** add generic gradient hero backgrounds.
- **Do not** add glassmorphism, neumorphism, or any 2020s design trend.
- **Do not** add unnecessary animations. Extra motion reads as AI-generated.
- **Do not** swap fonts or colors without owner approval.

---

## Self-critique checkpoint

Before Phase 3 begins, build chat must ask itself: *"Does this design plan read as a choice made for this specific brief, or as a generic construction-website template?"* If it reads generic in any section, revise before writing code, and note what was changed and why in `DECISIONS.md`.

---

**Status: LOCKED.**
