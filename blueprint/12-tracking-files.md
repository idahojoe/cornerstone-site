# 12 — Tracking Files

Claude Code maintains these four files at the repo root. Build chat proposes updates; Claude Code writes them.

---

## `STATUS.md`

**Purpose:** Snapshot of where the project is right now. Any new chat or contributor reads this first.

**Structure:**
```markdown
# Status

**Current phase:** Phase X — [name]
**Last updated:** YYYY-MM-DD

## Done
- Phase 1: Scaffold ✅
- Phase 2: Global styles ✅

## In progress
- Phase 3: Home page — hero built, tagline added, need button styling

## Blockers
- Waiting on owner for logo (expected [date])
- Waiting on owner for professional email address

## Next
- Complete Phase 3, seek owner approval, move to Phase 4
```

**Update rule:** At the end of every phase, and any time a blocker appears or resolves.

---

## `DECISIONS.md`

**Purpose:** Every locked decision. Prevents re-litigating settled questions.

**Structure:**
```markdown
# Decisions

## From blueprint (locked before build started)
- Stack: static HTML/CSS/JS. No frameworks. [Source: 01-project.md]
- Palette: sawdust, pine-shadow, iron-rust, concrete, sagebrush. [Source: 03-design.md]
- Fonts: Fraunces, Inter, Space Mono. [Source: 03-design.md]
- (etc — copied from blueprint)

## New decisions made during build
- YYYY-MM-DD — Phase 2: Adjusted --color-accent from #8B3A1F to #8E3E22 to pass WCAG AA contrast on cream background. Approved by owner.
- YYYY-MM-DD — Phase 3: Selected Unsplash photo [URL] as hero image. Compressed to 478 KB. Approved by owner.
```

**Update rule:** Any time a decision is made or an existing one is modified.

---

## `CHANGELOG.md`

**Purpose:** Running log of what changed and when. Reverse chronological.

**Structure:**
```markdown
# Changelog

## 2026-08-25
- Phase 3 complete — home page built and approved.
- Hero image added: hero-home.jpg (478 KB).

## 2026-08-24
- Phase 2 complete — global styles, nav, footer, buttons.
- Verified WCAG AA color contrast on all token pairs.

## 2026-08-23
- Phase 1 complete — repo scaffolded.
- Blueprint folder committed for reference.
```

**Update rule:** After every phase, and after any content or design change.

---

## `README.md`

**Purpose:** How to use, update, and maintain this site. Written for the owner, not for developers.

**Structure:**
```markdown
# Jackson & Grear Cornerstone Construction — Website

The website for Jackson & Grear Cornerstone Construction.

## Live site
[URL once deployed]

## How to update

### Change text on a page
1. Open the .html file for the page you want to change.
2. Edit the text.
3. Commit and push. Live in ~30 seconds.

### Swap a photo
1. Go to /images/ and find the photo.
2. Delete it.
3. Upload the new photo with the SAME filename.
4. Commit and push.

### Add a project photo
1. Compress the photo to under 300 KB (use squoosh.app).
2. Name it project-XX.jpg (next number in sequence).
3. Upload to /images/projects/.
4. Add an <img> tag to projects.html.
5. Commit and push.

### Update phone or email
1. Search across all .html files for the old value.
2. Replace everywhere.
3. Commit and push.

## Backup
Once a month: GitHub → Code → Download ZIP. Save to Google Drive or personal computer.

## Blueprint
The full planning blueprint is in /blueprint/. Read it before making major changes.
```

**Update rule:** Any time a workflow changes or a new type of update becomes common.

---

**Status: LOCKED.**
