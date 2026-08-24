# Decisions

## From blueprint (locked before build started)
- Stack: static HTML/CSS/JS only. No frameworks, no build tools, no CMS, no backend. [Source: 01-project.md]
- Hosting: GitHub Pages, auto-deploy from `main`. [Source: 01-project.md]
- Pages: 5 pages (Home, Services, Projects, About, Contact) + 404.html, robots.txt, sitemap.xml. [Source: 10-golden-rules.md]
- Palette: sawdust cream (#F2EDE0), pine-shadow ink (#1C2620), weathered iron rust (#8B3A1F / #6B2A15), concrete gray (#6E6A5F), sagebrush green (#8A8F72). [Source: 03-design.md]
- Fonts: Fraunces (display), Inter (body), Space Mono or JetBrains Mono (utility). No substitutions. [Source: 03-design.md]
- Layout: mobile-first, spacious, max content width 1200px. [Source: 03-design.md]
- Content: all page copy locked verbatim. [Source: 02-pages-content.md]
- Photos: filename-based swaps only, never hardcode paths that break on replacement. [Source: 05-photos.md]
- No scope creep: no contact forms, blog, CMS, analytics, cookie banners, third-party widgets, social embeds unless approved. [Source: 10-golden-rules.md]
- Execution split: build chat proposes, Claude Code executes all file writes. [Source: 10-golden-rules.md]
- Phased workflow: 9 phases, in order, stop for approval between each. [Source: 11-build-workflow.md]

## New decisions made during build
- 2026-08-24 — Phase 1: Used bare working titles (e.g. "Home — Jackson & Grear") for all page `<title>` tags; full SEO titles from 06-seo-social.md deferred to Phases 3–7. Per owner instruction.
- 2026-08-24 — Phase 1 setup: JetBrains Mono selected over Space Mono for utility font. Reason: better legibility at small sizes (nav caps), more distinctive character shape, less overused. Approved by owner. Will be formalized in Phase 2 when style.css is written; 03-design.md remains as-is until then.
- 2026-08-24 — Phase 2: Added `--color-focus: #80856A` token (darkened sagebrush) for focus outlines. Locked `--color-sage` (#8A8F72) measured 2.87:1 against `--color-base`, below the 3:1 WCAG 1.4.11 non-text minimum. New token verified at 3.28:1 on `--color-base` and 4.07:1 on `--color-ink`. Approved by owner.
- 2026-08-24 — Phase 2: Footer links render in `--color-base` text with a `--color-accent` underline (not solid rust text), because rust text directly on the `--color-ink` footer background measured 2.02:1 — well below the 4.5:1 text requirement. Hover/focus flips text color to `--color-accent`. Approved by owner.
- 2026-08-24 — Phase 2: Sticky header uses a solid `--color-base` background with a 1px `--color-secondary` bottom border — no `backdrop-filter`/translucency. Reason: blur reads as a generic modern-web-app pattern, undercuts the "grounded, working outfit" brief. Approved by owner.
- 2026-08-24 — Phase 2: Signature divider — Variant 2 ("stamped ruler ticks") selected over Variant 1 ("chalk-line snap"). Reason: reinforces the "stamped on equipment" aesthetic already established by the mono nav. Variant 1 discarded. Approved by owner. CSS (`.section-divider`) is in place; SVG markup itself is not placed on any page until Phase 3+.
- 2026-08-24 — Phase 2: Desktop nav breakpoint set at 1024px (medium breakpoint). Approved by owner.
- 2026-08-24 — Phase 2: Footer legal line uses `--color-base` at `opacity: 0.6` (rather than a raw hex/rgba) for a cleaner single-token approach. Approved by owner.
- 2026-08-24 — Phase 2: Hamburger menu implemented with a `<button>` + minimal JS (`js/script.js`), not a CSS-only checkbox hack. Reason: native checkboxes only toggle via Space, not Enter, in every major browser, and `07-accessibility.md` locks "Enter or Space" as a requirement. Golden-rules-tier accessibility requirement takes precedence over `08-performance.md`'s softer "prefer CSS if clean" preference. Approved by owner.
