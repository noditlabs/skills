# getWebhook

> Get Webhook

- **Category**: Webhook API
- **Official Docs**: https://developer.nodit.io/reference/getWebhook

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

`GET /{chain}/{network}/webhooks`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`, `arbitrum`, `arc`, `base`, `bnb`, `ethereum`, `giwa`, `kaia`, `optimism`, `polygon`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `testnet`, `sepolia`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Query Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `subscriptionId` | string | No | Webhook subscriptionId parameter . Webhook creation subscriptionId Webhook , . value input Webhook . |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |


## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `total` | number | Yes | event . |
| `page` | number | Yes | number. |
| `rpp` | number | Yes | event . |

**Items Schema:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `subscriptionId` | string | Yes | Webhook subscriptionId field. subscriptionId Webhook value , Webhook , . |
| `description` | string | Yes | Webhook field. |
| `protocol` | string | Yes | Webhook chain field. (e.g., ETHEREUM, POLYGON, OPTIMISM, ...) |
| `network` | string | Yes | Webhook network field. (e.g., MAINNET, SEPOLIA, MUMBAI, ...) |
| `subscriptionType` | string | Yes | 구독 유형을 식별할 수 있는 필드입니다. |
| `eventType` | string | Yes | Webhook event field. |
| `notification` | object | Yes | Webhook field. |
| `isInstant` | boolean | No | Instant Webhook . - true: event finalized event Webhook . - false: event transaction finalized . |
| `isActive` | boolean | Yes | Webhook field. Webhook true, false . Webhook Webhook . |
| `updatedAt` | string | Yes | result(status) . , . ISO 8601 . |
| `createdAt` | string | Yes | event creation . ISO 8601 . |
| `condition` | object | Yes | Webhook field. event . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
