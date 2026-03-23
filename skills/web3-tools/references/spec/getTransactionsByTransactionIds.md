# getTransactionsByTransactionIds

> Get Transactions By Transaction IDs

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/getTransactionsByTransactionIds

## Supported Chains

- bitcoin
- bitcoincash
- dogecoin

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/blockchain/getTransactionsByTransactionIds`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `bitcoin`, `bitcoincash`, `dogecoin`. Default: `bitcoin`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionIds` | array | Yes | transaction ID array input. |

## Response

### Success (200) - Successful Response

**Bitcoin (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `vin` | object | No |  |
| `vout` | object | No |  |

**Bitcoin Cash (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `vin` | object | No |  |
| `vout` | object | No |  |

**Dogecoin (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `vin` | object | No |  |
| `vout` | object | No |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
