# updateWebhook

> Update an existing EVM webhook's subscription conditions, activate or deactivate it, or change its notification URL and description.

- **Category**: Webhook API
- **Official Docs**: https://developer.nodit.io/reference/updateWebhook

## Supported Chains
- Arbitrum (mainnet, sepolia)
- Base (mainnet, sepolia)
- BNB (mainnet)
- Ethereum (mainnet, sepolia, hoodi)
- Giwa (sepolia)
- Kaia (mainnet, kairos)
- Optimism (mainnet, sepolia)
- Polygon (mainnet, amoy)

## Endpoint
`PATCH /{chain}/{network}/webhooks/{subscriptionId}`

## Parameters / Request Body

### Path Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `chain` | string | Yes | Target chain. Enum: `arbitrum`, `base`, `bnb`, `ethereum`, `giwa`, `kaia`, `optimism`, `polygon` |
| `network` | string | Yes | Target network. Enum: `mainnet`, `testnet`, `sepolia`, `hoodi`, `amoy` (varies by chain) |
| `subscriptionId` | string | Yes | The subscription ID of the webhook to update |

### Request Body (application/json)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `notification` | object | No | Notification configuration |
| `notification.webhookUrl` | string | No | New publicly accessible webhook URL |
| `description` | string | No | Updated description |
| `isActive` | boolean | No | Set `true` to activate, `false` to deactivate |
| `condition` | object | No | Updated subscription conditions |

#### Condition types (same as createWebhook):

- **ADDRESS_ACTIVITY**: `addresses` (string[])
- **MINED_TRANSACTION**: `addresses` (string[])
- **SUCCESSFUL_TRANSACTION**: `addresses` (string[])
- **FAILED_TRANSACTION**: `addresses` (string[])
- **TOKEN_TRANSFER**: `tokens` (object[] with `contractAddress`, optional `tokenId`)
- **BELOW_THRESHOLD_BALANCE**: `address` (string), `belowThresholdBalance` (string)
- **BLOCK_PERIOD**: `period` (integer)
- **BLOCK_LIST_CALLER**: `address` (string), `blockListCallers` (string[])
- **ALLOW_LIST_CALLER**: `address` (string), `allowListCallers` (string[])
- **LOG**: `address` (string), `topics` (string[], 1-4 items)

## Response

### 200 Successful Response

| Field | Type | Description |
|-------|------|-------------|
| `result` | boolean | `true` on success, `false` on failure |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | INVALID_PARAMETER | Bad request |
| 401 | AUTHENTICATION_FAILED | Unauthorized |
| 403 | PERMISSION_DENIED | Forbidden |
| 404 | RESOURCE_NOT_FOUND | Not found |
| 429 | TOO_MANY_REQUESTS | Rate limited |
