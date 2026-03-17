# getNativeTransfersWithinRange

> Get Native Transfers Within Range

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getNativeTransfersWithinRange

## Supported Chains

- arc
- tron

Networks: testnet, mainnet

## Endpoint

`POST /{chain}/{network}/native/getNativeTransfersWithinRange`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `arc`, `tron`. Default: `arc`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `testnet`, `mainnet`. Default: `testnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Tron

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | object | No |  |


## Response

### Success (200) - Successful Response

**Arc:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Tron:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
