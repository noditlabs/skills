# getInternalTransactionsByTransactionHash

> Retrieve internal transactions for a specific transaction hash on EVM chains and Tron.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getInternalTransactionsByTransactionHash

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, tron
- Networks: mainnet

## Endpoint
`POST /{chain}/{network}/blockchain/getInternalTransactionsByTransactionHash`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| transactionHash | string | Yes | Transaction hash. EVM: 0x-prefixed 64-char hex. Tron: 64-char hex (no prefix). |
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
| traceId | string | Trace ID |
| traceIndex | integer | Trace index |
| transactionHash | string | Transaction hash |
| transactionIndex | string | Transaction index in block |
| from | string | Sender address |
| to | string | Receiver address |
| value | string | Transferred amount |
| traceType | string | Trace type (call, create) |
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
| internalTransactionIndex | integer | Internal tx index in block |
| transactionHash | string | Parent transaction hash |
| transactionIndex | integer | Parent tx index |
| blockNumber | integer | Block number |
| blockTimestamp | integer | Block timestamp (milliseconds) |
| rejected | boolean | Whether the internal tx failed |
| from | string | Sender address |
| to | string | Receiver address |
| callValueInfo | array | Array of {value, assetId} |
| note | string | Operation type |
| extra | string | Additional data |
