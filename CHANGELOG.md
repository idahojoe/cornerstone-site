# Changelog

## 2026-08-26
- Phase 8b Part 1 complete — headless source audit across all six pages (index, services, projects, about, contact, 404) plus `css/style.css` and `js/script.js`; two findings identified (footer link hover contrast, nav link tap targets undersized); non-issues dismissed (JSON-LD subtype, divider hash reference artifact) — see DECISIONS.md.
- Phase 8c complete — CSS fixes for footer link hover contrast and nav link tap targets, approved by owner; `css/style.css` only, no HTML changes — see DECISIONS.md.
- Font swap complete — display font changed site-wide from Fraunces to Libre Caslon Text due to Fraunces capital-J descender reading as distracting at hero size; `css/style.css`, all six HTML pages, and `blueprint/03-design.md` updated — see DECISIONS.md.

## 2026-08-25
- Phase 8a complete — custom 404 page built and approved.
- New CSS Section 17 (`.not-found`) appended to `style.css`.
- Blueprint housekeeping: `06-seo-social.md` Services meta description synced to 5-category scope.

## 2026-08-24
- Services content expansion complete — 5 categories with expanded scope, new Seasonal & Property Care category with bulleted sub-list, updated head metadata (see DECISIONS.md).

## 2026-08-24
- Phase 7 complete — contact page built and approved.
- Removed "Email coming soon" line from contact page visible content (see DECISIONS.md).
- Revised contact page phone number font to JetBrains Mono for stronger design voice (see DECISIONS.md).

## 2026-08-24
- Phase 6 complete — about page built and approved.
- Revised Jeremiah Jackson bio paragraph for plainer voice (see DECISIONS.md).

## 2026-08-24
- Phase 5 complete — projects page approved by owner.
- Phase 5 in progress — projects page built, awaiting owner approval to close out phase.
- Phase 5: `projects.html` — full SEO head (title, meta description, canonical placeholder, Open Graph, Twitter card; no JSON-LD), h1 "Recent Work", empty gallery grid ready for `/images/projects/` photos, centered empty-state placeholder message ("New projects coming soon — check back."), instructional HTML comment documenting how to add a photo (including the `onerror` broken-image handler), two signature dividers (intro→gallery, gallery→CTA), "Call for an Estimate" CTA button.
- Phase 5: `css/style.css` — added Section 14 (Projects): intro centering, responsive gallery grid (1/2/3 columns at 640px/1024px breakpoints), gallery item box (aspect-ratio, object-fit, neutral background/border for missing photos), empty-state message styling, centered CTA.
- Phase 4 complete — services page approved by owner.
- Phase 4 in progress — services page built, awaiting owner approval to close out phase.
- Phase 4: `services.html` — full SEO head (title, meta description, canonical placeholder, Open Graph, Twitter card; no JSON-LD), h1 "What We Build", four services with locked copy (New Construction, Remodels & Additions, Concrete & Foundations, Repairs & Replacements), two signature dividers (intro→list, list→CTA), "Call for an Estimate" CTA button.
- Phase 4: `css/style.css` — added Section 13 (Services): intro centering, single-column services list with generous gaps, service block max-width, centered CTA.
- Phase 3 complete — home page built and approved by owner.
- Phase 3: Hero image added — `images/hero/hero-home.jpg` (Alex Moliski, "Fog rolls in over a misty Idaho mountain morning," Sawtooth National Forest, Idaho; Unsplash License). Cropped to 16:9, resized to 1920×1080, compressed to 244,033 bytes (~238 KB).
- Phase 3: `index.html` — full SEO head (title, meta description, canonical placeholder, Open Graph, Twitter card, LocalBusiness JSON-LD), hero section (image, 35% ink overlay, company name, tagline, tap-to-call phone, "Call for an Estimate" button), signature divider (stamped ruler ticks SVG, first concrete markup for the Phase 2 concept), service area line.
- Phase 3: `css/style.css` — added Section 12 (Hero); added `height: 16px` to the existing `.section-divider` rule in Section 8.
- Phase 2 complete — global styles approved by owner.
- Phase 2: global styles written — css/style.css (11 sections: tokens, reset, typography, layout primitives, nav, footer, buttons, signature divider, skip-link/utility, print, reduced-motion).
- Phase 2: hamburger toggle written to js/script.js.
- Phase 2: all 6 HTML shells updated with full head (fonts, stylesheet), skip-link, shared nav (aria-current per page), empty main, shared footer, deferred script tag.
- Phase 2: two accessibility contrast issues found beyond the blueprint's named pairs (sage focus outline on base, rust text on ink footer) and fixed — see DECISIONS.md.
- Phase 1 complete — scaffold approved by owner.
- Repo scaffolded: 6 HTML shells, css/js placeholders, robots.txt, sitemap.xml, .gitignore, .gitkeep files, blueprint folder copied in, tracking files initialized.
- Initial git commit made locally. No remote configured yet.
