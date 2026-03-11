# SEO Rules

Use this as the minimum technical baseline for static sites.

## Metadata

- Add one descriptive `<title>` per page. Target roughly 45-60 characters.
- Add one `meta[name="description"]` per page. Target roughly 120-155 characters.
- Add one canonical URL per indexable page.
- Add `meta[name="robots"]` only when needed. Default to indexable pages unless the task says otherwise.
- Keep Open Graph and Twitter metadata aligned with the page title, description, canonical URL, and social image.

## Semantics

- Keep exactly one meaningful `<h1>` per page.
- Use `h2` and `h3` to reflect real content sections, not visual styling alone.
- Wrap page content in semantic landmarks where practical: `header`, `main`, `nav`, `section`, `article`, `footer`.
- Add descriptive `alt` text to content images. Leave decorative images empty with `alt=""`.

## Crawlability

- Ensure important pages are reachable through internal links.
- Add `robots.txt` for multi-page sites.
- Add `sitemap.xml` for multi-page sites and include canonical URLs only.
- Avoid orphan pages, broken canonical targets, and links to non-existent routes.

## Content Alignment

- Keep metadata consistent with visible content.
- Prefer clear search intent over keyword stuffing.
- Use natural language variations of the primary topic instead of repeating one exact phrase.
- If the page is local-intent, include city, region, or service area naturally in the visible copy.

## Safe Defaults

- Preserve stronger existing metadata if it is already accurate.
- Remove duplicate or contradictory tags before inserting replacements.
- Do not add `noindex`, `nofollow`, or crawl blocking unless explicitly requested.
- Do not add schema that the visible page content cannot support.
