# syncNftMetadata

> Sync Nft Metadata

- **Category**: Data API - NFT
- **Official Docs**: https://developer.nodit.io/reference/syncNftMetadata

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

Networks: mainnet, sepolia, testnet, hoodi, kairos, amoy

## Endpoint

`POST /{chain}/{network}/nft/syncNftMetadata`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`. Default: `arbitrum`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |


## Response

### Success (200) - Successful Response

**Arbitrum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

**Arc:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

**Base:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

**BNB Smart Chain:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

**Chiliz:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

**Ethereum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

**Ethereum Classic:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

**Giwa:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

**Kaia:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

**Luniverse:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

**Optimism:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

**Polygon:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `message` | string | No | result is returned. |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
