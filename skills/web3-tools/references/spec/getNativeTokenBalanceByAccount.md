# getNativeTokenBalanceByAccount

> Get Native Token Balance by Account

- **Category**: Data API - Token

## Supported Chains

- bitcoin
- bitcoincash
- dogecoin
- xrpl

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/native/getNativeTokenBalanceByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `bitcoin`, `bitcoincash`, `dogecoin`, `xrpl`. Default: `bitcoin`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter. |

## Response

### Success (200) - Successful Response

**Bitcoin:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |

**XRP Ledger:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address , 25~35 Base58 encoding "r" . |
| `balance` | string | Yes | , XRP drop XRP (1 XRP =1,000,000 drop) value . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
