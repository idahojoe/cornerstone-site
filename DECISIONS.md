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
