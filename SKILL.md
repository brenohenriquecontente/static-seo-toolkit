---
name: static-seo-toolkit
description: Create, review, and repair technical SEO for static websites and landing pages built with HTML, CSS, JavaScript, or static site generators. Use when adding or fixing title tags, meta descriptions, canonical URLs, Open Graph and Twitter cards, JSON-LD structured data, robots.txt, sitemap.xml, heading hierarchy, internal linking, image alt text, or local business SEO for single-page or multi-page static sites.
---

# Static SEO Toolkit

## Overview

Use this skill to turn a static site or HTML brief into an indexable, shareable, SEO-safe site structure without introducing backend dependencies.
Prefer minimal, deterministic improvements that preserve the site's design while fixing crawlability, metadata, semantics, and local-intent gaps.

## Workflow

1. Classify the task.

- New site from a brief: build the page structure and metadata baseline before polishing copy.
- Existing site audit: inspect current HTML and enumerate SEO defects before editing.
- Existing site revision: preserve useful SEO assets and replace only what is missing, invalid, duplicated, or contradictory.

2. Apply the baseline in [`references/seo-rules.md`](./references/seo-rules.md).

- Ensure exactly one descriptive `<title>` and one `meta[name="description"]` per page.
- Ensure one canonical URL per indexable page.
- Add Open Graph and Twitter card metadata that matches the page intent.
- Keep one meaningful `<h1>` and a coherent `h2`/`h3` hierarchy.
- Ensure important pages are internally linked and discoverable.
- Add `robots.txt` and `sitemap.xml` for multi-page sites unless the user explicitly wants pages blocked.

3. Choose structured data deliberately.

- Use `WebSite` on the site root when appropriate.
- Use `Organization`, `LocalBusiness`, or a more specific subtype for business homepages.
- Add `FAQPage` only when the page visibly contains FAQ content.
- Add `BreadcrumbList` only when the page sits in a navigable hierarchy.
- See [`references/schema-recipes.md`](./references/schema-recipes.md) and copy from `assets/jsonld/` only when it fits the visible page content.

4. Handle local business SEO when the business serves a city, district, or region.

- Use the business name, service, city, and region naturally in headings, copy, and metadata.
- Include NAP-style information when available: name, phone, address, service area, hours, socials.
- Prefer specific business schema over generic `Organization` when justified.
- See [`references/local-seo.md`](./references/local-seo.md).

5. Preserve and improve instead of duplicating.

- Remove duplicate canonical, OG, Twitter, or JSON-LD blocks before inserting replacements.
- Do not invent pages that are not linked, reachable, or supported by the site content.
- Do not add `noindex` or disallow crawling unless the user explicitly asks for it.
- Do not stuff keywords or add hidden text.
- Keep metadata aligned with the visible page content.

6. Deliver complete outputs.

- For a single page, return the corrected head markup and any required semantic/body fixes.
- For a multi-page site, also return or update `robots.txt`, `sitemap.xml`, and page-level canonicals.
- If information is missing, make the safest reasonable inference and say what should be confirmed.
- End with a short audit summary using [`references/audit-checklist.md`](./references/audit-checklist.md).

## Output Rules

- Keep the implementation static-first. Do not introduce a backend or dynamic SEO framework unless the user asks for it.
- Keep paths, canonicals, sitemap entries, and internal links consistent with the site's actual URL structure.
- If an existing site already has stronger metadata than your baseline, preserve it.
- Match metadata language to the page language.
- Prefer ASCII in templates unless the existing file already uses Unicode heavily.

## Resources

- Baseline rules: [`references/seo-rules.md`](./references/seo-rules.md)
- Local intent guidance: [`references/local-seo.md`](./references/local-seo.md)
- Schema selection and snippets: [`references/schema-recipes.md`](./references/schema-recipes.md)
- Final QA checklist: [`references/audit-checklist.md`](./references/audit-checklist.md)
- Reusable templates:
  - [`assets/head-template.html`](./assets/head-template.html)
  - [`assets/robots-template.txt`](./assets/robots-template.txt)
  - [`assets/sitemap-template.xml`](./assets/sitemap-template.xml)
  - [`assets/jsonld/organization.json`](./assets/jsonld/organization.json)
  - [`assets/jsonld/local-business.json`](./assets/jsonld/local-business.json)
  - [`assets/jsonld/faq-page.json`](./assets/jsonld/faq-page.json)

Load only the reference files needed for the current task. Do not bulk-load everything.
