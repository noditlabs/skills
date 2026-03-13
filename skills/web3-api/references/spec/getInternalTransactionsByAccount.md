# getInternalTransactionsByAccount

> Retrieve internal transactions associated with a specific account on EVM chains and Tron.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getInternalTransactionsByAccount

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, tron
- Networks: mainnet

## Endpoint
`POST /{chain}/{network}/blockchain/getInternalTransactionsByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | Yes | Account address (EVM: 0x-prefixed 40-char hex; Tron: T-prefixed 34-char base58) |
| relation | string | No | Filter: `from`, `to`, or `both` (default: both) |
| fromBlock | string | No | Start block (number, hash, or tag) |
| toBlock | string | No | End block (number, hash, or tag) |
| fromDate | string | No | Start date (ISO 8601) |
| toDate | string | No | End date (ISO 8601) |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (1-1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count (default: false) |
| withZeroValue | boolean | No | EVM only. Include zero-value results (default: false) |
| withExternalTransaction | boolean | No | EVM only. Include external transactions (default: false) |

## Response

### 200 OK - EVM (Paginated)

Items contain:

| Field | Type | Description |
|-------|------|-------------|
| traceId | string | Trace ID (format: call_{block}_{txIndex}_{depths}) |
| traceIndex | integer | Trace index (0 for external transactions) |
| transactionHash | string | Transaction hash |
| transactionIndex | string | Transaction index in block |
| from | string | Sender address |
| to | string | Receiver address |
| value | string | Transferred amount |
| traceType | string | Trace type (call, create, etc.) |
| callType | string | Call type (call, delegatecall, staticcall) |
| gas | string | Allocated gas |
| gasUsed | string | Gas used |
| status | string | Status (1=success, 0=failure) |
| blockNumber | integer | Block number |
| timeStamp | integer | Unix timestamp |

### 200 OK - Tron (Paginated)

Items contain:

| Field | Type | Description |
|-------|------|-------------|
| internalTransactionHash | string | Internal transaction hash |
| internalTransactionIndex | integer | Internal transaction index in block |
| transactionHash | string | Parent transaction hash |
| transactionIndex | integer | Parent transaction index |
| blockNumber | integer | Block number |
| blockTimestamp | integer | Block timestamp (milliseconds) |
| rejected | boolean | Whether the internal tx failed |
| from | string | Sender address |
| to | string | Receiver address |
| callValueInfo | array | Array of {value, assetId} |
| note | string | Operation type (call, create, etc.) |
| extra | string | Additional data |
