# getNftHoldersByTokenId

> Retrieve the list of holders for a specific NFT token ID, including holder addresses and balances.

- **Category**: Data API - NFT
- **Official Docs**: https://developer.nodit.io/reference/getNftHoldersByTokenId

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

`POST /{chain}/{network}/nft/getNftHoldersByTokenId`

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
| `contractAddress` | string | Yes | Contract address (0x-prefixed, 40 hex chars) |
| `tokenId` | string | Yes | NFT token ID as a decimal string |
| `page` | integer | No | Page number (1-100). Cannot be used with `cursor` |
| `rpp` | integer | No | Results per page (1-1000) |
| `cursor` | string | No | Cursor for pagination. Cannot be used with `page` |
| `withCount` | boolean | No | Include total count in response. Default: `false` |

## Response

### 200 - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | Current page number |
| `rpp` | integer | No | Results per page |
| `cursor` | string | No | Cursor for next page |
| `count` | integer | No | Total count (only if `withCount` is true) |
| `items` | array | Yes | List of holder records |

**Items array element:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | Holder's address (0x-prefixed, 40 hex chars) |
| `totalBalance` | string | Yes | Total balance for this token ID |
| `uniqueBalance` | string | Yes | Unique token ID count |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
