# getNftsOwnedByAccount

> Retrieve all NFTs owned by a specific account, including token balances, metadata, and contract information.

- **Category**: Data API - NFT
- **Official Docs**: https://developer.nodit.io/reference/getNftsOwnedByAccount

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

`POST /{chain}/{network}/nft/getNftsOwnedByAccount`

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
| `accountAddress` | string | Yes | Account address (0x-prefixed, 40 hex chars) |
| `contractAddresses` | string[] | No | Filter by specific contract addresses |
| `page` | integer | No | Page number (1-100). Cannot be used with `cursor` |
| `rpp` | integer | No | Results per page (1-1000) |
| `cursor` | string | No | Cursor for pagination |
| `withCount` | boolean | No | Include total count. Default: `false` |
| `withMetadata` | boolean | No | Include NFT rawMetadata and metadataSyncedAt. Default: `false` |

## Response

### 200 - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | Current page number |
| `rpp` | integer | No | Results per page |
| `cursor` | string | No | Cursor for next page |
| `count` | integer | No | Total count (only if `withCount` is true) |
| `items` | array | Yes | List of owned NFTs |

**Items array element:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | Owner's address |
| `balance` | string | Yes | Token balance (decimal string) |
| `lastTransferredAt` | string | Yes | Last transfer time in ISO 8601 format |
| `tokenId` | string | Yes | Unique token ID |
| `tokenUri` | string | Yes | URI pointing to the NFT's metadata |
| `tokenUriSyncedAt` | string | Yes | When the tokenUri was last synced |
| `rawMetadata` | string | No | Raw metadata JSON (only if `withMetadata` is true) |
| `metadataSyncedAt` | string | No | Metadata sync time (only if `withMetadata` is true) |
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
