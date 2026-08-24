# 11 — Build Workflow

**Rules:**
- Phases run in order.
- No skipping.
- No combining.
- No touching the next phase until owner approves the current one.
- Claude Code writes files; build chat proposes and reviews.
- At the end of each phase, Claude Code updates `STATUS.md` and `CHANGELOG.md`.

---

## Phase 1 — Scaffold

**What happens:**
- Create folder structure per `04-file-structure.md`.
- Create empty `index.html`, `services.html`, `projects.html`, `about.html`, `contact.html`, `404.html`.
- Create empty `css/style.css`, `js/script.js`.
- Create `robots.txt`, `sitemap.xml`, `.gitignore`.
- Create `README.md`, `STATUS.md`, `DECISIONS.md`, `CHANGELOG.md`.
- Copy the entire `/blueprint/` folder into the repo for reference.

**Deliverable:** Repo is scaffolded. Nothing rendered yet.

→ **STOP. AWAIT APPROVAL.**

---

## Phase 2 — Global Styles

**What happens:**
- Build chat re-reads `03-design.md`, `07-accessibility.md`, `08-performance.md`.
- Build chat runs the self-critique checkpoint from `03-design.md`.
- Set up CSS custom properties for all color and type tokens.
- Load Google Fonts (Fraunces, Inter, Space Mono/JetBrains Mono) with `display=swap`.
- Build shared nav bar, footer, button styles.
- Build reset / base styles.
- Set up mobile breakpoints.
- Verify color contrast meets WCAG AA. Document verification in `DECISIONS.md`.

**Deliverable:** All pages inherit the design system. Nav and footer visible on any page.

→ **STOP. AWAIT APPROVAL.**

---

## Phase 3 — Home Page

**What happens:**
- Select and download Idaho landscape from Unsplash. Compress to under 500 KB. Save as `/images/hero/hero-home.jpg`.
- Build hero section per `03-design.md`.
- Add tagline, phone (tap-to-call), "CALL FOR AN ESTIMATE" button.
- Add service area line below hero.
- Add signature divider element.
- Add SEO tags (title, meta description, Open Graph) per `06-seo-social.md`.
- Add `LocalBusiness` JSON-LD.

**Deliverable:** Home page fully built, live-preview ready.

→ **STOP. AWAIT APPROVAL.**

---

## Phase 4 — Services Page

**What happens:**
- Build services page with all 4 categories, locked blurbs from `02-pages-content.md`.
- "CALL FOR AN ESTIMATE" button at bottom.
- Add SEO tags.

**Deliverable:** Services page fully built.

→ **STOP. AWAIT APPROVAL.**

---

## Phase 5 — Projects Page

**What happens:**
- Build empty gallery grid structure.
- Placeholder note: "New projects coming soon — check back."
- Prepared to accept photos dropped into `/images/projects/`.
- "CALL FOR AN ESTIMATE" button at bottom.
- Add SEO tags.

**Deliverable:** Projects page fully built, ready for photos.

→ **STOP. AWAIT APPROVAL.**

---

## Phase 6 — About Page

**What happens:**
- Build with locked About copy from `02-pages-content.md`.
- "CALL FOR AN ESTIMATE" button at bottom.
- Add SEO tags.

**Deliverable:** About page fully built.

→ **STOP. AWAIT APPROVAL.**

---

## Phase 7 — Contact Page

**What happens:**
- Build contact page.
- Prominent "CALL FOR AN ESTIMATE" button near top.
- Phone (tap-to-call).
- Email placeholder.
- Service area.
- Add SEO tags.

**Deliverable:** Contact page fully built.

→ **STOP. AWAIT APPROVAL.**

---

## Phase 8 — 404 Page + Mobile QA

**What happens:**
- Build custom `404.html` matching site style. Says "Page not found" with link back to home and phone number.
- Test every page at 375px width (iPhone), 768px (tablet), 1280px (desktop).
- Fix anything broken.
- Verify hamburger menu works on mobile.
- Verify tap-to-call and tap-to-email work.
- Verify keyboard navigation works.
- Run through accessibility checklist in `07-accessibility.md`.

**Deliverable:** All pages work on mobile, tablet, desktop. 404 page in place.

→ **STOP. AWAIT APPROVAL.**

---

## Phase 9 — Deploy

**What happens:**
- Verify all tracking files (`STATUS.md`, `DECISIONS.md`, `CHANGELOG.md`, `README.md`) are current.
- Push to GitHub.
- Enable GitHub Pages (deploy from `main` branch, `/` root).
- Confirm live URL works.
- Test live site on mobile.
- Update `sitemap.xml` and `robots.txt` with the live URL.

**Deliverable:** Site is LIVE.

→ **DONE.**

---

## Post-Launch (whenever ready — not phases, just tasks)

- **Logo received:** Swap text logo for image logo. Add favicon.
- **Domain purchased:** Add `CNAME` file at repo root. Update DNS. Update `sitemap.xml` and `robots.txt`.
- **Project photos added:** Drop into `/images/projects/`. Add `<img>` tags to `projects.html`.
- **Professional email set up:** Update contact page and footer.

---

**Status: LOCKED.**
