# getAccountStats

> Get Account Stats

- **Category**: Data API - Statistics
- **Official Docs**: https://developer.nodit.io/reference/getAccountStats

## Supported Chains

- arbitrum
- arc
- base
- bnb
- chiliz
- ethereum
- ethereumclassic
- giwa
- kaia
- luniverse
- optimism
- polygon
- tron
- aptos

Networks: mainnet, sepolia, testnet, hoodi, kairos, amoy

## Endpoint

`POST /{chain}/{network}/stats/getAccountStats`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`, `tron`, `aptos`. Default: `arbitrum`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | address parameter . 0x 40 hexadecimal string input . |

## Response

### Success (200) - Successful Response

**Arbitrum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionCounts` | object | No | address transaction object. |
| `transferCounts` | object | No | address event object. |
| `assets` | object | No | address object. |

**Tron:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionCounts` | object | No | address transaction object. |
| `transferCounts` | object | No | address event object. |
| `assets` | object | No | address object. |

**Aptos:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionCounts` | integer | Yes | creation transaction count field. sender transaction . |
| `balanceChangeCounts` | object | Yes |  |
| `assets` | object | Yes |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
