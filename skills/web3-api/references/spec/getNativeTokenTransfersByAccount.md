# getNativeTokenTransfersByAccount

> Retrieve native token transfer history for a specific account on UTXO-based chains (Bitcoin, Dogecoin, Bitcoincash).

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getNativeTokenTransfersByAccount

## Supported Chains
- bitcoin, dogecoin, bitcoincash
- Networks: mainnet

## Endpoint
`POST /{chain}/{network}/native/getNativeTokenTransfersByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (bitcoin, dogecoin, bitcoincash) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | Yes | Account address (P2PKH/P2SH/Bech32 format) |
| relation | string | No | Filter by sender/receiver: `from`, `to`, or `both` (default: both) |
| fromBlock | string | No | Start block (number, hash, or tag) |
| toBlock | string | No | End block (number, hash, or tag) |
| fromDate | string | No | Start date (ISO 8601) |
| toDate | string | No | End date (ISO 8601) |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (1-1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count (default: false) |

## Response

### 200 OK (Paginated)

Items contain:

| Field | Type | Description |
|-------|------|-------------|
| transactionHash | string | Transaction hash (64-char hex) |
| transactionId | string | Transaction ID (64-char hex) |
| blockHeight | integer | Block height |
| blockHash | string | Block hash |
| blockTimestamp | integer | Block creation time (Unix timestamp) |
| fee | string | Transaction fee in BTC |
| senders | array | Array of {index, address, value} |
| recipients | array | Array of {index, address, value} |
