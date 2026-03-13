# getTokenTransfersByContract

> Retrieve token transfer history for a specific contract. Includes contract metadata and transfer amounts.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenTransfersByContract

## Supported Chains

| Chain | Networks |
|-------|----------|
| arbitrum | mainnet, sepolia |
| base | mainnet, sepolia |
| bnb | mainnet, testnet |
| chiliz | mainnet, testnet |
| ethereum | mainnet, sepolia, hoodi |
| ethereumclassic | mainnet |
| giwa | mainnet |
| kaia | mainnet, testnet |
| optimism | mainnet, sepolia |
| polygon | mainnet, amoy |
| luniverse | mainnet |
| tron | mainnet, testnet |

## Endpoint

`POST /{chain}/{network}/token/getTokenTransfersByContract`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain. Enum: `arbitrum`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `optimism`, `polygon`, `luniverse`, `tron` |
| network | string | Yes | Target network. Enum: `mainnet`, `sepolia`, `hoodi`, `amoy`, `testnet` |

## Request Body

`Content-Type: application/json`

### EVM Chains

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| contractAddress | string | Yes | Contract address (0x + 40 hex chars). |
| fromBlock | string | No | Start block (number, hash, or tag). |
| toBlock | string | No | End block (number, hash, or tag). |
| fromDate | string | No | Start date (ISO 8601). Cannot be used with block params. |
| toDate | string | No | End date (ISO 8601). Cannot be used with block params. |
| withZeroValue | boolean | No | Include zero-value transfers. |
| withFunction | boolean | No | Include function call info. |

### Tron

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| contractAddress | string | Yes | Contract address (T + 33 base58 chars). |
| fromBlock | string | No | Start block. |
| toBlock | string | No | End block. |
| fromDate | string | No | Start date (ISO 8601). |
| toDate | string | No | End date (ISO 8601). |
| withZeroValue | boolean | No | Include zero-value transfers. |

### Pagination (both)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| page | integer | No | Page number (max 100). |
| rpp | integer | No | Results per page (1-1000). |
| cursor | string | No | Cursor for pagination. |
| withCount | boolean | No | Include total count. Default: `false`. |

## Response

### Success (200)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| page | integer | No | Page number. |
| rpp | integer | No | Results per page. |
| cursor | string | No | Cursor for next page. |
| count | integer | No | Total count (only if `withCount=true`). |
| items | array | Yes | List of transfer records. |

### Items Schema (EVM)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| from | string | Yes | Sender address. |
| to | string | Yes | Receiver address. |
| value | string | Yes | Transfer amount as decimal string. |
| timestamp | integer | Yes | Unix timestamp. |
| blockNumber | integer | Yes | Block number. |
| transactionHash | string | Yes | Transaction hash. |
| logIndex | integer | Yes | Event log index. |
| batchIndex | integer | No | Batch index (ERC1155 only). |
| function | object | No | Called function info (if `withFunction=true`). |
| contract | object | No | Contract metadata. |

### Items Schema (Tron)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| from | string | Yes | Sender address. |
| to | string | Yes | Receiver address. |
| value | string | Yes | Transfer amount. |
| blockTimestamp | integer | Yes | Block timestamp (milliseconds). |
| blockNumber | integer | Yes | Block number. |
| transactionHash | string | Yes | Transaction hash. |
| transactionIndex | integer | Yes | Transaction index in block. |
| logIndex | integer | No | Log index. |
| internalTransactionIndex | integer | No | Internal transaction index. |
| exchangeId | integer | No | DEX exchange ID. |
| contract | object | No | Contract metadata. |
