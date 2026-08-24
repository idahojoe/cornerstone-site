# 10 — Golden Rules

**These 12 rules are non-negotiable. The build chat cannot violate them. If any change is proposed, it requires explicit owner approval and must be logged in `DECISIONS.md`.**

---

1. **Stack:** Static HTML / CSS / JS only. No frameworks, no build tools, no npm, no CMS, no backend.

2. **Files:** One CSS file, one JS file (if needed), folder structure exactly as locked in `04-file-structure.md`.

3. **Pages:** 5 pages only — Home, Services, Projects, About, Contact. Plus `404.html`, `robots.txt`, `sitemap.xml`.

4. **Colors:** Use the exact token values from `03-design.md`. No new colors introduced without approval.

5. **Fonts:** Fraunces (display), Inter (body), Space Mono or JetBrains Mono (utility). No substitutions.

6. **Layout:** Spacious, mobile-first, responsive. Phone is tap-to-call. Email is tap-to-email.

7. **Photos:** Filename-based swaps. Never hardcode image references that break on replacement.

8. **Content:** Use locked copy from `02-pages-content.md` verbatim. No rewrites without approval.

9. **Hosting:** GitHub Pages. Domain-ready but not required at launch.

10. **No scope creep:** No contact forms, no blog, no CMS, no analytics, no cookie banners, no third-party widgets, no social embeds — unless approved.

11. **Execution split:** Build chat proposes and reviews. Claude Code executes all file creation, edits, and tracking-file updates. Build chat never writes to disk directly.

12. **Phased workflow:** Build chat follows `11-build-workflow.md` in order. No skipping. No combining. No jumping ahead. Full stop for owner approval between every phase.

---

**Status: LOCKED.**
