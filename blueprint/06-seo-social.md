# 06 — SEO & Social Sharing

---

## Page Titles (LOCKED)

Each page's `<title>` tag:

| Page | Title |
|---|---|
| Home | `Jackson & Grear Cornerstone Construction \| Boise County, Idaho` |
| Services | `Services \| Jackson & Grear Cornerstone Construction` |
| Projects | `Projects \| Jackson & Grear Cornerstone Construction` |
| About | `About \| Jackson & Grear Cornerstone Construction` |
| Contact | `Contact \| Jackson & Grear Cornerstone Construction` |
| 404 | `Page Not Found \| Jackson & Grear Cornerstone Construction` |

---

## Meta Descriptions (LOCKED)

One sentence per page. Google shows the first ~155 chars.

- **Home:** *Jackson & Grear Cornerstone Construction — new builds, remodels, concrete, and repairs in Boise County, Idaho. Serving Lowman, Garden Valley, and Stanley.*
- **Services:** *Services from Jackson & Grear Cornerstone Construction — new construction, remodels and additions, concrete and foundations, roofing, siding, and repairs.*
- **Projects:** *Recent projects from Jackson & Grear Cornerstone Construction, a small construction outfit in Boise County, Idaho.*
- **About:** *Meet Jeremiah Jackson and Joseph Grear — the partners behind Jackson & Grear Cornerstone Construction in Boise County, Idaho.*
- **Contact:** *Call Jackson & Grear Cornerstone Construction at 208-259-3387 for an estimate. Serving Lowman, Garden Valley, Stanley, and beyond.*

---

## Open Graph Tags (LOCKED)

Every page includes:

```html
<meta property="og:type" content="website">
<meta property="og:site_name" content="Jackson & Grear Cornerstone Construction">
<meta property="og:title" content="[same as page title]">
<meta property="og:description" content="[same as meta description]">
<meta property="og:image" content="/images/hero/hero-home.jpg">
<meta property="og:url" content="[canonical URL of this page]">
<meta name="twitter:card" content="summary_large_image">
```

**When someone shares a page in a text or on social:** shows a preview with the hero landscape image and the page title/description. Not blank, not broken.

---

## `robots.txt` (LOCKED)

At repo root:

```
User-agent: *
Allow: /
Sitemap: https://[domain]/sitemap.xml
```

Build chat updates the sitemap URL when domain is finalized.

---

## `sitemap.xml` (LOCKED)

At repo root. Lists all 5 pages:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url><loc>https://[domain]/</loc></url>
  <url><loc>https://[domain]/services.html</loc></url>
  <url><loc>https://[domain]/projects.html</loc></url>
  <url><loc>https://[domain]/about.html</loc></url>
  <url><loc>https://[domain]/contact.html</loc></url>
</urlset>
```

Update `[domain]` when live URL is known (first `*.github.io`, later `.com`).

---

## Structured Data (LOCKED — optional but included)

Add `LocalBusiness` schema.org JSON-LD to home page `<head>`. Helps Google show phone, address, and service area in local search results.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "GeneralContractor",
  "name": "Jackson & Grear Cornerstone Construction",
  "telephone": "+1-208-259-3387",
  "areaServed": ["Lowman, Idaho", "Garden Valley, Idaho", "Stanley, Idaho", "Boise County, Idaho"],
  "address": {
    "@type": "PostalAddress",
    "addressRegion": "ID",
    "addressCountry": "US"
  }
}
</script>
```

---

**Status: LOCKED.**
