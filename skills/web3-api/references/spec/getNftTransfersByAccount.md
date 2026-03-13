# getNftTransfersByAccount

> Retrieve NFT transfer history for a specific account, including sent and received transfers with contract and NFT metadata.

- **Category**: Data API - NFT
- **Official Docs**: https://developer.nodit.io/reference/getNftTransfersByAccount

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

`POST /{chain}/{network}/nft/getNftTransfersByAccount`

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
| `relation` | string | No | Filter by sender/receiver. Enum: `from`, `to`, `both`. Default: `both` |
| `contractAddresses` | string[] | No | Filter by specific contract addresses |
| `fromBlock` | string | No | Start block (block number, block hash, `earliest`, or `latest`). Cannot be used with `fromDate`/`toDate` |
| `toBlock` | string | No | End block (block number, block hash, `earliest`, or `latest`). Cannot be used with `fromDate`/`toDate` |
| `fromDate` | string | No | Start date in ISO 8601 format. Cannot be used with `fromBlock`/`toBlock` |
| `toDate` | string | No | End date in ISO 8601 format. Cannot be used with `fromBlock`/`toBlock` |
| `page` | integer | No | Page number (1-100). Cannot be used with `cursor` |
| `rpp` | integer | No | Results per page (1-1000) |
| `cursor` | string | No | Cursor for pagination |
| `withCount` | boolean | No | Include total count. Default: `false` |
| `withMetadata` | boolean | No | Include NFT rawMetadata and metadataSyncedAt. Default: `false` |
| `withZeroValue` | boolean | No | Include zero-value transfers. Default: `false` |
| `withFunction` | boolean | No | Include function call details. Default: `false` |

## Response

### 200 - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | Current page number |
| `rpp` | integer | No | Results per page |
| `cursor` | string | No | Cursor for next page |
| `count` | integer | No | Total count (only if `withCount` is true) |
| `items` | array | Yes | List of transfer records |

**Items array element:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `from` | string | Yes | Sender address |
| `to` | string | Yes | Receiver address |
| `value` | string | Yes | Transfer quantity (decimal string) |
| `timestamp` | integer | Yes | UNIX timestamp of the transfer |
| `blockNumber` | integer | Yes | Block number |
| `transactionHash` | string | Yes | Transaction hash |
| `logIndex` | integer | Yes | Log index in the transaction |
| `batchIndex` | integer | No | Batch index (ERC1155 only) |
| `contract` | object | No | Contract metadata (address, name, symbol, type, etc.) |
| `nft` | object | No | NFT metadata (tokenId, tokenUri, tokenUriSyncedAt, rawMetadata*, metadataSyncedAt*) |
| `function` | object | No | Function call info (only if `withFunction` is true). Contains: selector, name, signature, args, input |

*rawMetadata and metadataSyncedAt only included when `withMetadata` is true.

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
