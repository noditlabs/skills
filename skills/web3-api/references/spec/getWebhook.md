# getWebhook

> Retrieve webhook information by Subscription ID. Returns a paginated list of webhooks for the specified chain and network.

- **Category**: Webhook API
- **Official Docs**: https://developer.nodit.io/reference/getWebhook

## Supported Chains
- Arbitrum (mainnet, sepolia)
- Base (mainnet, sepolia)
- BNB (mainnet)
- Ethereum (mainnet, sepolia, hoodi)
- Kaia (mainnet, kairos)
- Optimism (mainnet, sepolia)
- Polygon (mainnet, amoy)
- Aptos (mainnet, testnet)

## Endpoint
`GET /{chain}/{network}/webhooks`

## Parameters / Request Body

### Path Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `chain` | string | Yes | Target chain. Enum: `arbitrum`, `base`, `bnb`, `ethereum`, `kaia`, `optimism`, `polygon`, `aptos` |
| `network` | string | Yes | Target network. Enum: `mainnet`, `testnet`, `sepolia`, `hoodi`, `amoy` (varies by chain) |

### Query Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `subscriptionId` | string | No | Filter by specific subscription ID. If empty, returns all webhooks. |

## Response

### 200 Successful Response

| Field | Type | Description |
|-------|------|-------------|
| `total` | number | Total number of matching events |
| `page` | number | Current page number |
| `rpp` | number | Results per page |
| `items` | array | Array of webhook objects |

#### Webhook Item

| Field | Type | Description |
|-------|------|-------------|
| `subscriptionId` | string | Unique webhook identifier |
| `description` | string | Webhook description |
| `protocol` | string | Subscribed chain (e.g., ETHEREUM) |
| `network` | string | Subscribed network (e.g., MAINNET) |
| `subscriptionType` | string | Subscription type (e.g., `WEBHOOK`) |
| `eventType` | string | Subscribed event type |
| `notification` | object | Contains `webhookUrl` |
| `isInstant` | boolean | Whether instant webhook is enabled |
| `isActive` | boolean | Whether webhook is active |
| `updatedAt` | string | Last update timestamp (ISO 8601) |
| `createdAt` | string | Creation timestamp (ISO 8601) |
| `condition` | object | Subscription conditions |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | INVALID_PARAMETER | Bad request |
| 401 | AUTHENTICATION_FAILED | Unauthorized |
| 403 | PERMISSION_DENIED | Forbidden |
| 404 | RESOURCE_NOT_FOUND | Not found |
| 429 | TOO_MANY_REQUESTS | Rate limited |
