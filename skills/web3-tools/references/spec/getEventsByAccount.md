# getEventsByAccount

> Get Events by Account

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/getEventsByAccount

## Supported Chains

- aptos

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/blockchain/getEventsByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`. Default: `aptos`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | account address parameter . account address 64 hexadecimal("0x" ) input . |
| `eventTypes` | array | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

## Response

### Success (200) - Successful Response

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
