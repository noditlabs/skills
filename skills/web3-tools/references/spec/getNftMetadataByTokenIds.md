# getNftMetadataByTokenIds

> Get NFT Metadata by Token IDs

- **Category**: Data API - NFT

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

`POST /{chain}/{network}/nft/getNftMetadataByTokenIds`

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

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokens` | array | Yes | NFT . 100 . |

## Response

### Success (200) - Successful Response

**Arbitrum (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

**Arc (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

**Base (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

**BNB Smart Chain (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

**Chiliz (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

**Ethereum (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

**Ethereum Classic (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

**Giwa (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

**Kaia (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

**Luniverse (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

**Optimism (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

**Polygon (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | Yes | NFT rawMetadata field. |
| `metadataSyncedAt` | string | Yes | NFT metadata field. |
| `contract` | object | No |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
