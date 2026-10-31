# OptiSigns

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

OptiSigns is a cloud digital signage platform that turns any TV or display into a digital sign using low-cost media players (Android, Amazon Fire TV, Raspberry Pi, ProDVX, and others). Screens, media assets, playlists, and schedules are managed centrally from the OptiSigns dashboard. Developers manage the same resources programmatically through the OptiSigns GraphQL API, which is served from a single endpoint at https://graphql-gateway.optisigns.com/graphql and authenticated with a Bearer API key. API access is a paid capability available on the Pro Plus plan and higher; the API covers devices (screens), assets (content), playlists, schedules, and team management. Official TypeScript/JavaScript and Python SDKs plus an API cookbook are published on GitHub.

**Areas:** Digital Signage · Screens · Content Management · GraphQL · Displays · Playlists

## OptiSigns on APIs.io

Everything profiled for OptiSigns is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/optisigns/](https://apis.io/providers/optisigns/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [OptiSigns Devices API](https://apis.io/apis/optisigns/optisigns-devices-api/) — Query and manage the devices (screens) paired to an OptiSigns account. List devices, look them up by name or ID, create and update device settings, reboot a…
- [OptiSigns Assets API](https://apis.io/apis/optisigns/optisigns-assets-api/) — Manage the content assets displayed on screens - upload file assets (images, video, documents), create website and app assets, modify asset settings, list…
- [OptiSigns Playlists API](https://apis.io/apis/optisigns/optisigns-playlists-api/) — Create and manage playlists - ordered sequences of assets with per-item durations - and assign them to devices. Playlists are a documented OptiSigns…
- [OptiSigns Schedules API](https://apis.io/apis/optisigns/optisigns-schedules-api/) — Create and manage schedules that control when assets and playlists play on which devices across dates, times, and recurrence. Schedules are a documented…
- [OptiSigns Teams API](https://apis.io/apis/optisigns/optisigns-teams-api/) — Organize devices and assets into teams (sub-accounts) for multi-location and multi-tenant management. Teams are a documented OptiSigns resource type…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### GraphQL (1)

GraphQL schemas.

- [OptiSigns GraphQL API](https://apis.io/graphqls/optisigns/optisigns-graphql/)

#### Collections (1)

Postman and Open Collection request collections.

- [OptiSigns GraphQL API](https://apis.io/collections/optisigns/open-optisigns/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Optisigns Domain Security](https://apis.io/security/optisigns/optisigns-domain-security/)
- [Optisigns Trust Center](https://apis.io/security/optisigns/optisigns-trust-center/)
- [Optisigns Vulnerability Disclosure](https://apis.io/security/optisigns/optisigns-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Optisigns Plans Pricing](https://apis.io/plans/optisigns/optisigns-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Optisigns Rate Limits](https://apis.io/rate-limits/optisigns/optisigns-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Optisigns Finops](https://apis.io/finops/optisigns/optisigns-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.optisigns.com)
- [Documentation](https://docs.optisigns.com)
- [Blog](https://www.optisigns.com/blog)
- [GitHub](https://github.com/optisigns)

## API Evangelist rating

**Kin Score 18.0** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 71.4 |
| Contract quality | 0.0 |
| Contract governance | 0.0 |
| Operational transparency | 10.5 |
| Developer ergonomics | 30.5 |
| Access clarity | 15.8 |

**Agent readiness 0.6** — human-only

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 16.7** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/optisigns/](https://apis.io/providers/optisigns/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for OptiSigns: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/optisigns/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
