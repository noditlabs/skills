# createWebhook

> Create Webhook

- **Category**: Webhook API

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

`POST /{chain}/{network}/webhooks`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`, `arbitrum`, `arc`, `base`, `bnb`, `ethereum`, `giwa`, `kaia`, `optimism`, `polygon`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `testnet`, `sepolia`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `eventType` | object | Yes |  |
| `description` | string | No | event parameter. |
| `notification` | object | Yes | event parameter. |
| `isInstant` | boolean | No | Instant Webhook parameter , false . - true: Instant Webhook , finalized event Webhook . - false: Instant Webhook , event transaction finalized . |
| `condition` | object | Yes |  |

## Response

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
