# OptiSigns (optisigns)

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
