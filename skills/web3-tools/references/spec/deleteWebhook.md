# deleteWebhook

> Delete Webhook

- **Category**: Webhook API
- **Official Docs**: https://developer.nodit.io/reference/deleteWebhook

## Supported Chains

- aptos
- arbitrum
- arc
- base
- bnb
- ethereum
- giwa
- kaia
- optimism
- polygon

Networks: mainnet, testnet, sepolia, hoodi, kairos, amoy

## Endpoint

`DELETE /{chain}/{network}/webhooks/{subscriptionId}`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`, `arbitrum`, `arc`, `base`, `bnb`, `ethereum`, `giwa`, `kaia`, `optimism`, `polygon`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `testnet`, `sepolia`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |
| `subscriptionId` | string | Yes | Webhook subscriptionId parameter . Webhook creation subscriptionId Webhook , . |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |


## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | result field. true, false is returned. |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
