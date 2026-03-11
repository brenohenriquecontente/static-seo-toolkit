# Static SEO Toolkit

Open source workflow and template pack for building, auditing, and repairing technical SEO on static websites.

It is designed for developers working with:

- plain HTML/CSS/JS sites
- static landing pages
- exported sites from visual builders
- static site generators where the final output is still page-based HTML

## What it helps with

- generate or fix page titles and meta descriptions
- add canonical URLs
- add Open Graph and Twitter card metadata
- choose and apply JSON-LD safely
- improve heading hierarchy and semantic structure
- add `robots.txt` and `sitemap.xml`
- strengthen local business SEO for service-area sites
- preserve SEO while editing an existing static site

## Skill structure

```text
static-seo-toolkit/
├── SKILL.md
├── agents/openai.yaml
├── references/
│   ├── seo-rules.md
│   ├── local-seo.md
│   ├── schema-recipes.md
│   └── audit-checklist.md
└── assets/
    ├── head-template.html
    ├── robots-template.txt
    ├── sitemap-template.xml
    └── jsonld/
```

## Suggested use cases

- "Use $static-seo-toolkit to audit this multi-page static site."
- "Use $static-seo-toolkit to add SEO tags and schema to this landing page."
- "Use $static-seo-toolkit to improve local SEO for a clinic website in one city."

## Publishing

If you publish this as its own repository, keep this folder as the repo root so the package remains easy to consume and inspect.

Suggested repo topics:

- `seo`
- `static-site`
- `html`
- `technical-seo`
- `json-ld`

## License

MIT
