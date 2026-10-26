# OptiSigns (optisigns)

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

OptiSigns is a cloud digital signage platform that turns any TV or display into a digital sign using low-cost media players (Android, Amazon Fire TV, Raspberry Pi, ProDVX, and others). Screens, media assets, playlists, and schedules are managed centrally from the OptiSigns dashboard, and the same resources can be managed programmatically through the OptiSigns GraphQL API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/optisigns/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/optisigns/refs/heads/main/apis.yml)

## Access Model (Read This First)

The OptiSigns API is a **paid, self-serve capability** - not open, and not available on every plan.

- **Protocol:** GraphQL only. There is a single endpoint at `https://graphql-gateway.optisigns.com/graphql`. OptiSigns does **not** publish a traditional REST API. A web-based GraphQL IDE is available at the same URL for exploring the schema.
- **Authentication:** API key sent as an HTTP header, `Authorization: Bearer YOUR_KEY_HERE`. Keys are generated in the dashboard at `https://app.optisigns.com/generate-api-key` (also reachable from Account Settings).
- **Plan requirement:** GraphQL API access is included on the **Pro Plus** plan ($15/screen/month, or $13.50 paid annually) and higher, including **Enterprise** ($45/screen/month, or $40.50 annually, minimum 25 screens). Lower tiers (Free, Standard, Pro) and their per-screen pricing do not include API access. Third-party pricing summaries sometimes describe API access as Enterprise-only; OptiSigns' own pricing page lists it from Pro Plus up. Confirm the current entitlement for your account on the [pricing page](https://www.optisigns.com/pricing) before building.
- **No public WebSocket / realtime API.** The public surface is request/response GraphQL over HTTPS. See `review.yml`.

## APIs

Five logical APIs are modeled over the single GraphQL endpoint. Device and Asset operations are **confirmed** against the official OptiSigns Node SDK; Playlist, Schedule, and Team operations are documented resource types whose exact GraphQL fields are **honestly modeled** and flagged in the schema.

### OptiSigns Devices API

Query and manage the devices (screens) paired to an account: list, look up by name or ID, create, update, reboot, push content, and delete. Confirmed SDK methods: `listAllDevices`, `findByDeviceName`, `getDeviceById`, `createDevice`, `updateDevice`, `deleteDeviceById`, `rebootDevice`, `pushContentToDevice`.

- **Human URL:** [https://docs.optisigns.com/quickstart](https://docs.optisigns.com/quickstart)
- **Base URL:** `https://graphql-gateway.optisigns.com/graphql`

### OptiSigns Assets API

Manage content assets shown on screens: upload file assets (images, video, documents), create website/app assets, modify settings, list and fetch by filename, and delete. Confirmed SDK methods: `uploadFileAsset`, `createWebsiteAppAsset`, `modifyAssetSettings`, `deleteAssetById`.

- **Human URL:** [https://docs.optisigns.com/quickstart](https://docs.optisigns.com/quickstart)
- **Base URL:** `https://graphql-gateway.optisigns.com/graphql`

### OptiSigns Playlists API

Create and manage playlists - ordered sequences of assets with per-item durations - and assign them to devices. **Operations modeled** from the documented resource type.

- **Human URL:** [https://docs.optisigns.com/quickstart](https://docs.optisigns.com/quickstart)
- **Base URL:** `https://graphql-gateway.optisigns.com/graphql`

### OptiSigns Schedules API

Create and manage schedules that control when assets and playlists play on which devices across dates, times, and recurrence. **Operations modeled** from the documented resource type.

- **Human URL:** [https://docs.optisigns.com/quickstart](https://docs.optisigns.com/quickstart)
- **Base URL:** `https://graphql-gateway.optisigns.com/graphql`

### OptiSigns Teams API

Organize devices and assets into teams (sub-accounts) for multi-location and multi-tenant management. **Operations modeled** from the documented resource type.

- **Human URL:** [https://docs.optisigns.com/quickstart](https://docs.optisigns.com/quickstart)
- **Base URL:** `https://graphql-gateway.optisigns.com/graphql`

## Tags

- Digital Signage
- Screens
- Content Management
- GraphQL
- Displays
- Playlists

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## Common Properties

- [GitHub Organization](https://github.com/optisigns)
- [LinkedIn](https://www.linkedin.com/company/optisigns)
- [Website](https://www.optisigns.com)
- [Documentation](https://docs.optisigns.com)
- [Plans](plans/optisigns-plans-pricing.yml)
- [Rate Limits](rate-limits/optisigns-rate-limits.yml)
- [FinOps](finops/optisigns-finops.yml)
- [SDK](https://github.com/optisigns/optisigns-node)

## Sources

- Quickstart: [https://docs.optisigns.com/quickstart](https://docs.optisigns.com/quickstart)
- API section (support): [https://support.optisigns.com/hc/en-us/sections/4414558217235-OptiSigns-API](https://support.optisigns.com/hc/en-us/sections/4414558217235-OptiSigns-API)
- Generate & Manage API Key: [https://support.optisigns.com/hc/en-us/articles/4414563797139-Generate-Manage-OptiSigns-API-Key](https://support.optisigns.com/hc/en-us/articles/4414563797139-Generate-Manage-OptiSigns-API-Key)
- Official Node SDK: [https://github.com/optisigns/optisigns-node](https://github.com/optisigns/optisigns-node)
- API Cookbook: [https://github.com/optisigns/optisigns-api-cookbook](https://github.com/optisigns/optisigns-api-cookbook)
- Pricing: [https://www.optisigns.com/pricing](https://www.optisigns.com/pricing)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
