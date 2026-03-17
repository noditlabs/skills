# getDailyTransactionsStats

> Get Daily Transactions Stats

- **Category**: Data API - Statistics
- **Official Docs**: https://developer.nodit.io/reference/getDailyTransactionsStats

## Supported Chains

- ethereum
- luniverse

Networks: mainnet, sepolia, hoodi

## Endpoint

`POST /{chain}/{network}/stats/getDailyTransactionsStats`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `ethereum`, `luniverse`. Default: `ethereum`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `hoodi`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `startDate` | string | Yes | parameter . 100 data . YYYY-MM-DD . |
| `endDate` | string | Yes | parameter . 100 data . YYYY-MM-DD . |

## Response

### Success (200) - Successful Response

**Ethereum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `count` | integer | No | data field. withCount parameter true input . |
| `items` | array | Yes |  |

**Luniverse:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `count` | integer | No | data field. withCount parameter true input . |
| `items` | array | Yes |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
