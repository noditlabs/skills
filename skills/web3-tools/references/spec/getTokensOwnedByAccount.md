# getTokensOwnedByAccount

> Get Tokens Owned By Account

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokensOwnedByAccount

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

`POST /{chain}/{network}/token/getTokensOwnedByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`, `tron`, `aptos`. Default: `arbitrum`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

### Arbitrum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Base

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### BNB Smart Chain

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Chiliz

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Ethereum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Ethereum Classic

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Giwa

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Kaia

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Luniverse

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Optimism

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Polygon

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Tron

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `contractAddresses` | object | No |  |

### Aptos

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | account address parameter . account address 64 hexadecimal("0x" ) input . |
| `assetTypes` | array | No |  |
| `linkedAssetTypes` | array | No |  |


## Response

### Success (200) - Successful Response

**Arbitrum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Arc:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Base:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**BNB Smart Chain:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Chiliz:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Ethereum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Ethereum Classic:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Giwa:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Kaia:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Luniverse:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Optimism:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Polygon:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Tron:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Aptos:**

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
