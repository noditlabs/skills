# getNftHoldersByTokenId

> Get NFT Holders by Token ID

- **Category**: Data API - NFT
- **Official Docs**: https://developer.nodit.io/reference/getNftHoldersByTokenId

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

`POST /{chain}/{network}/nft/getNftHoldersByTokenId`

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

## Request Body

`Content-Type: application/json`

### Arbitrum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |

### Base

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |

### BNB Smart Chain

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |

### Chiliz

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |

### Ethereum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |

### Ethereum Classic

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |

### Giwa

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |

### Kaia

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |

### Luniverse

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |

### Optimism

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |

### Polygon

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `tokenId` | string | Yes | NFT token ID parameter . 10 input . |


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

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
