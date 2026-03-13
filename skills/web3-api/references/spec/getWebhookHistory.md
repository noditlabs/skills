# getWebhookHistory

> Retrieve the call history of a webhook. Returns execution status and detailed results for each webhook invocation. History data is retained for 30 days only.

- **Category**: Webhook API
- **Official Docs**: https://developer.nodit.io/reference/getWebhookHistory

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
`GET /{chain}/{network}/webhooks/history`

## Parameters / Request Body

### Path Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `chain` | string | Yes | Target chain. Enum: `arbitrum`, `base`, `bnb`, `ethereum`, `kaia`, `optimism`, `polygon`, `aptos` |
| `network` | string | Yes | Target network. Enum: `mainnet`, `testnet`, `sepolia`, `hoodi`, `amoy` (varies by chain) |

### Query Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `subscriptionId` | string | Yes | Subscription ID to query history for. If empty, returns all webhook history. |
| `page` | string | No | Page number (default: 1) |
| `rpp` | string | No | Results per page, 1-100 (default: 10) |
| `withEventMessage` | boolean | No | Include event message data (default: false) |
| `status` | string | No | Filter by status. Enum: `SUCCESS`, `FAIL` |
| `startAt` | string | No | Start time filter (ISO 8601) |
| `endAt` | string | No | End time filter (ISO 8601) |
| `startSequenceNumber` | string | No | Starting sequence number for pagination |

## Response

### 200 Successful Response

| Field | Type | Description |
|-------|------|-------------|
| `total` | number | Total number of matching events |
| `page` | number | Current page number |
| `rpp` | number | Results per page |
| `items` | array | Array of history entries |

#### History Item

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | History entry ID |
| `subscriptionId` | string | Webhook subscription ID |
| `sequenceNumber` | string | Sequence number of the event |
| `status` | string | Delivery status (`SUCCESS` or `FAIL`) |
| `updatedAt` | string | Last status change timestamp (ISO 8601) |
| `createdAt` | string | Event creation timestamp (ISO 8601) |
| `eventMessage` | object | Event message details (when `withEventMessage=true`) |

#### Event Message (when included)

| Field | Type | Description |
|-------|------|-------------|
| `subscriptionId` | string | Webhook subscription ID |
| `sequenceNumber` | string | Sequence number |
| `eventType` | string | Event type |
| `network` | string | Network |
| `protocol` | string | Protocol/chain |
| `event` | object | Event-specific data |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | INVALID_PARAMETER | Bad request |
| 401 | AUTHENTICATION_FAILED | Unauthorized |
| 403 | PERMISSION_DENIED | Forbidden |
| 404 | RESOURCE_NOT_FOUND | Not found |
| 429 | TOO_MANY_REQUESTS | Rate limited |
