# OptiSigns GraphQL API

OptiSigns is a cloud digital signage platform. Its public developer API is **GraphQL only** - there is no REST API. All operations run against a single endpoint, and the same URL serves an interactive GraphQL IDE for exploring the schema.

**Endpoint:** `https://graphql-gateway.optisigns.com/graphql`
**Authentication:** API key as an HTTP header - `Authorization: Bearer YOUR_KEY_HERE`
**API keys:** Generated in the dashboard at `https://app.optisigns.com/generate-api-key` (also under Account Settings)
**Documentation:** https://docs.optisigns.com

## Access

GraphQL API access is a paid capability included on the **Pro Plus** plan ($15/screen/month, $13.50 annually) and higher, including **Enterprise** ($45/screen/month, $40.50 annually, minimum 25 screens). Free, Standard, and Pro tiers do not include API access. Confirm current entitlement on https://www.optisigns.com/pricing.

## Operations

GraphQL splits into **Query** (read) and **Mutation** (write) operations. The schema in `optisigns-schema.graphql` models five resource groups:

- **Devices (screens)** - CONFIRMED against the official Node SDK: `listAllDevices`, `findByDeviceName`, `getDeviceById`, `createDevice`, `updateDevice`, `deleteDeviceById`, `rebootDevice`, `pushContentToDevice`.
- **Assets (content)** - CONFIRMED against the official Node SDK: `uploadFileAsset`, `createWebsiteAppAsset`, `modifyAssetSettings`, `deleteAssetById`.
- **Playlists** - MODELED. Documented resource type; exact field names not published.
- **Schedules** - MODELED. Documented resource type; exact field names not published.
- **Teams** - MODELED. Documented resource type; exact field names not published.

Fields and operations marked `MODELED` in the schema are honestly reconstructed from the documented resource types and the SDK/cookbook surface; verify exact names against the live GraphQL IDE and current schema introspection before building against them.

## Example

```graphql
# List all paired devices (screens)
query {
  devices(first: 25) {
    edges {
      node {
        id
        deviceName
        uuid
        pairingCode
        appVersion
        currentAssetId
        currentPlaylistId
      }
    }
  }
}
```

```bash
curl -s https://graphql-gateway.optisigns.com/graphql \
  -H "Authorization: Bearer YOUR_KEY_HERE" \
  -H "Content-Type: application/json" \
  -d '{"query":"{ devices(first: 25) { edges { node { id deviceName uuid } } } }"}'
```

- Reference: https://support.optisigns.com/hc/en-us/sections/4414558217235-OptiSigns-API
- SDK: https://github.com/optisigns/optisigns-node
- Cookbook: https://github.com/optisigns/optisigns-api-cookbook
- Schema: https://github.com/api-evangelist/optisigns
