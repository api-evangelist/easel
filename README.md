# Easel AI

Easel AI is a Los Angeles based generative AI company. Its models turn a single selfie into photorealistic single and multiplayer avatars with no per-user AI training, and package that capability for brands as Fashion Photoshoot, Fashion Try-On, Ad Creator, and Product Photoshoot. Easel ships a consumer iOS app and markets its APIs to fashion brands, ad platforms, messaging apps, dating and social apps, and talent agencies.

- Website: https://easelapps.ai/
- iOS app: https://apps.apple.com/us/app/easel-ai/id6448734086
- Contact: hello@easelapps.ai
- Backed by: a16z (appears on the a16z investment list)

## API status: partner-gated, no public developer surface

Easel explicitly markets APIs — the site says "Looking to partner on our APIs?", "Fashion brands can integrate Try-On API on their website or styling app", and "Ad platforms can integrate Easel's API". But as of the 2026-07-20 enrichment pass, none of it is public. Verified absent:

| Surface | Result |
| --- | --- |
| Developer portal / docs / API reference | none published |
| OpenAPI / AsyncAPI / GraphQL spec | none |
| Self-serve signup, pricing, sandbox | none |
| SDKs / packages (npm, PyPI checked) | none first-party |
| CLI, changelog, status page, roadmap | none |
| `/.well-known/*`, `llms.txt`, `robots.txt`, `sitemap.xml` | none — see below |
| Public GitHub org | unconfirmed (see note) |
| Vulnerability disclosure program / trust center | none found |

`easelapps.ai` is a single-page app on Azure Static Web Apps that returns the SPA shell (HTTP 200, `text/html`) for every unmatched path, so every discovery probe is a soft-404. `well-known/easel-well-known.yml` records this honestly rather than treating the 200s as hits.

**GitHub note:** `github.com/easel-ai` exists ("Empowering artists and businesses with advanced image editing tools") but has 0 public repos and lists `easel.ai` as its site — a domain now parked and for sale. The link to `easelapps.ai` could not be confirmed, so no `GitHubOrganization` pointer was emitted.

## Artifacts in this repo

- `well-known/easel-well-known.yml` — discovery probe results (all soft-404, searched)
- `llms/easel-llms.txt` — generated llms.txt from the catalog + site copy
- `security/easel-domain-security.yml` — probed TLS 1.3, HSTS (max-age 10886400), DNSSEC on, no SPF, DMARC `p=none`, no CAA

## Next pass

Re-check for a developer portal, docs, or a published Try-On API reference. The commercial framing (contact sales for API partnership) suggests a private beta that may open up.
