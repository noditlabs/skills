# isContract

> Is Contract

- **Category**: Data API - Blockchain

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

Networks: mainnet, sepolia, testnet, hoodi, kairos, amoy

## Endpoint

`POST /{chain}/{network}/blockchain/isContract`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`, `tron`. Default: `arbitrum`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

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
| `result` | boolean | No | input Address contract true, false is returned. |

**Arc:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

**Base:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

**BNB Smart Chain:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

**Chiliz:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

**Ethereum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

**Ethereum Classic:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

**Giwa:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

**Kaia:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

**Luniverse:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

**Optimism:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

**Polygon:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

**Tron:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `result` | boolean | No | input Address contract true, false is returned. |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
