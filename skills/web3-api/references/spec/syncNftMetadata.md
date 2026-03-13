# syncNftMetadata

> Trigger a metadata sync for specific NFTs. Supports batch sync of up to 100 NFTs. Sync may take up to 10 seconds to complete.

- **Category**: Data API - NFT
- **Official Docs**: https://developer.nodit.io/reference/syncNftMetadata

## Supported Chains

- arbitrum
- base
- bnb
- chiliz
- ethereum
- ethereumclassic
- giwa
- kaia
- optimism
- polygon
- luniverse

## Endpoint

`POST /{chain}/{network}/nft/syncNftMetadata`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Target blockchain. Enum: `arbitrum`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `optimism`, `polygon`, `luniverse`. Default: `ethereum` |
| `network` | string | Yes | Target network. Enum: `mainnet`, `sepolia`, `hoodi`, `amoy`, `testnet`. Default: `mainnet` |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo: `nodit-demo` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokens` | array | Yes | Array of token identifiers to sync (max 100) |

**tokens array element:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | Contract address (0x-prefixed, 40 hex chars) |
| `tokenId` | string | Yes | Token ID as a decimal string |

## Response

### 200 - Successful Response

| Field | Type | Description |
|-------|------|-------------|
| `message` | string | Confirmation message, e.g., "NFT Metadata synchronization request has been successfully submitted." |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
