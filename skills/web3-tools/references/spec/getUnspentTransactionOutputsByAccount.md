# getUnspentTransactionOutputsByAccount

> Get Unspent Transaction Outputs By Account

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/getUnspentTransactionOutputsByAccount

## Supported Chains

- bitcoin
- bitcoincash
- dogecoin

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/blockchain/getUnspentTransactionOutputsByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `bitcoin`, `bitcoincash`, `dogecoin`. Default: `bitcoin`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

### Bitcoin

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |

### Bitcoin Cash

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |

### Dogecoin

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |


## Response

### Success (200) - Successful Response

**Bitcoin:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Bitcoin Cash:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Dogecoin:**

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
