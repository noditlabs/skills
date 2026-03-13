# getNativeTransfersWithinRange

> Retrieve native token transfers within a specified time or block range on Tron.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getNativeTransfersWithinRange

## Supported Chains
- tron
- Networks: mainnet

## Endpoint
`POST /{chain}/{network}/native/getNativeTransfersWithinRange`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (tron) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| fromBlock | string | No | Start block (number, hash, or tag) |
| toBlock | string | No | End block (number, hash, or tag) |
| fromDate | string | No | Start date (ISO 8601) |
| toDate | string | No | End date (ISO 8601) |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (1-1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count (default: false) |
| withZeroValue | boolean | No | Include zero-value transfers (default: false) |

## Response

### 200 OK (Paginated)

Items contain:

| Field | Type | Description |
|-------|------|-------------|
| from | string | Sender address |
| to | string | Receiver address |
| value | string | Transfer amount |
| blockTimestamp | integer | Block timestamp (milliseconds Unix) |
| blockNumber | integer | Block number |
| transactionHash | string | Transaction hash |
| transactionIndex | integer | Transaction position in block |
| logIndex | integer | Log index |
| internalTransactionIndex | integer | Internal tx index (-1 = root transaction) |
| exchangeId | integer | DEX exchange ID (null if not a swap) |
