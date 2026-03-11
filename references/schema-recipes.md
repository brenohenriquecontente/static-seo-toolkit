# Schema Recipes

Choose the narrowest schema that matches the visible page content.

## Common Choices

- `WebSite`: site root or general website identity
- `Organization`: companies without strong local business signals
- `LocalBusiness`: businesses with location or service-area signals
- `ProfessionalService`: agencies, consultants, law firms, studios, service businesses
- `MedicalClinic`: clinics and healthcare practices
- `Restaurant`: restaurants, cafes, bars
- `Store`: ecommerce or local retail
- `FAQPage`: only when the page visibly includes FAQs
- `BreadcrumbList`: only when the page lives in a clear hierarchy

## Selection Rules

- Do not stack unrelated top-level schemas on the same page without a reason.
- Keep names, URLs, phone numbers, and addresses consistent with visible page content.
- Use `sameAs` only for real profile URLs.
- Use a page URL for the entity's `url` when the entity is primarily represented on that page.

## Asset Snippets

- Base organization: [`../assets/jsonld/organization.json`](../assets/jsonld/organization.json)
- Local business: [`../assets/jsonld/local-business.json`](../assets/jsonld/local-business.json)
- FAQ page: [`../assets/jsonld/faq-page.json`](../assets/jsonld/faq-page.json)
