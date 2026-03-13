# getNftMetadataByTokenIds

> Retrieve metadata for specific NFTs by their contract address and token ID pairs. Supports batch lookup of up to 100 NFTs.

- **Category**: Data API - NFT
- **Official Docs**: https://developer.nodit.io/reference/getNftMetadataByTokenIds

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

`POST /{chain}/{network}/nft/getNftMetadataByTokenIds`

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
| `tokens` | array | Yes | Array of token identifiers (max 100) |

**tokens array element:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | Contract address (0x-prefixed, 40 hex chars) |
| `tokenId` | string | Yes | Token ID as a decimal string |

## Response

### 200 - Successful Response

Returns an array of NFT metadata objects:

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `tokenId` | string | Yes | Unique token ID |
| `tokenUri` | string | Yes | URI pointing to the NFT's metadata |
| `tokenUriSyncedAt` | string | Yes | When the tokenUri was last synced |
| `rawMetadata` | string | Yes | Raw metadata JSON string |
| `metadataSyncedAt` | string | Yes | When the metadata was last synced |
| `contract` | object | No | Contract metadata |

**Contract object:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | Contract address |
| `deployedTransactionHash` | string | Yes | Deployment transaction hash |
| `deployedAt` | string | Yes | Deployment time (ISO 8601) |
| `deployerAddress` | string | Yes | Deployer address |
| `logoUrl` | string \| null | Yes | Contract logo URL |
| `type` | string | Yes | Contract type (ERC721, ERC1155) |
| `name` | string | Yes | Contract name |
| `symbol` | string | Yes | Contract symbol |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
