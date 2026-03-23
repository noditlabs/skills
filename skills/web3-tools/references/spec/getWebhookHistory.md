# getWebhookHistory

> Get Webhook History

- **Category**: Webhook API
- **Official Docs**: https://developer.nodit.io/reference/getWebhookHistory

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

`GET /{chain}/{network}/webhooks/history`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`, `arbitrum`, `arc`, `base`, `bnb`, `ethereum`, `giwa`, `kaia`, `optimism`, `polygon`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `testnet`, `sepolia`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Query Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `subscriptionId` | string | Yes | Webhook subscriptionId parameter . Webhook creation subscriptionId Webhook , . value input Webhook . |
| `page` | string | No | is specified. value 1. |
| `rpp` | string | No | event is specified. value 1 100 . value 10. |
| `withEventMessage` | boolean | No | event is specified. value false. |
| `status` | string | No | (SUCCESS) (FAIL) event filter . Enum: `SUCCESS`, `FAIL`. |
| `startAt` | string | No | event ISO 8601 . |
| `endAt` | string | No | event ISO 8601 . |
| `startSequenceNumber` | string | No | sequenceNumber is specified. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |


## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `total` | number | No | event . |
| `page` | number | No | number. |
| `rpp` | number | No | event . |

**Items Schema:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `subscriptionId` | string | No | Webhook subscriptionId field. subscriptionId Webhook value , Webhook , . |
| `description` | string | No | Webhook field. |
| `protocol` | string | No | Webhook chain field. (e.g., ETHEREUM, POLYGON, OPTIMISM, ...) |
| `network` | string | No | Webhook network field. (e.g., MAINNET, SEPOLIA, MUMBAI, ...) |
| `subscriptionType` | string | No | 구독 유형을 식별할 수 있는 필드입니다. |
| `eventType` | string | No | Webhook event field. |
| `notification` | object | No | Webhook field. |
| `isActive` | boolean | No | Webhook field. Webhook true, false . Webhook Webhook . |
| `updatedAt` | string | No | result(status) . , . ISO 8601 . |
| `createdAt` | string | No | event creation . ISO 8601 . |
| `condition` | object | No | Webhook field. event . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
