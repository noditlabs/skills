# deleteWebhook

> Delete a webhook subscription. Once deleted, the webhook subscription is cancelled and no further events will be delivered.

- **Category**: Webhook API
- **Official Docs**: https://developer.nodit.io/reference/deleteWebhook

## Supported Chains
- Arbitrum (mainnet, sepolia)
- Base (mainnet, sepolia)
- BNB (mainnet)
- Ethereum (mainnet, sepolia, hoodi)
- Giwa (sepolia)
- Kaia (mainnet, kairos)
- Optimism (mainnet, sepolia)
- Polygon (mainnet, amoy)
- Aptos (mainnet, testnet)

## Endpoint
`DELETE /{chain}/{network}/webhooks/{subscriptionId}`

## Parameters / Request Body

### Path Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `chain` | string | Yes | Target chain. Enum: `arbitrum`, `base`, `bnb`, `ethereum`, `giwa`, `kaia`, `optimism`, `polygon`, `aptos` |
| `network` | string | Yes | Target network. Enum: `mainnet`, `testnet`, `sepolia`, `hoodi`, `amoy` (varies by chain) |
| `subscriptionId` | string | Yes | The subscription ID of the webhook to delete |

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
