# Easel AI

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
