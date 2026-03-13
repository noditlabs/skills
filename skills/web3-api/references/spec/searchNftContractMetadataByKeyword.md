# searchNftContractMetadataByKeyword

> Search for NFT contracts by matching a keyword against contract name or symbol.

- **Category**: Data API - NFT
- **Official Docs**: https://developer.nodit.io/reference/searchNftContractMetadataByKeyword

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

`POST /{chain}/{network}/nft/searchNftContractMetadataByKeyword`

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
| `keyword` | string | Yes | Search keyword to match against token name or symbol |
| `page` | integer | No | Page number (1-100). Cannot be used with `cursor` |
| `rpp` | integer | No | Results per page (1-1000) |
| `cursor` | string | No | Cursor for pagination |
| `withCount` | boolean | No | Include total count. Default: `false` |

## Response

### 200 - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | Current page number |
| `rpp` | integer | No | Results per page |
| `cursor` | string | No | Cursor for next page |
| `count` | integer | No | Total count (only if `withCount` is true) |
| `items` | array | Yes | List of matching contracts |

**Items array element:**

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
