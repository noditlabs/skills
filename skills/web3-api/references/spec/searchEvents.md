# searchEvents

> Search for specific smart contract events within a block or date range on EVM chains.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/searchEvents

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse
- Networks: mainnet, testnet, sepolia, hoodi, amoy

## Endpoint
`POST /{chain}/{network}/blockchain/searchEvents`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| contractAddress | string | Yes | Contract address (0x-prefixed, 40-char hex) |
| eventNames | array | Yes | Array of event names to search for (e.g., ["Transfer"]) |
| abi | string | Yes | Contract ABI in JSON format |
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
| contractAddress | string | Contract that emitted the event |
| transactionHash | string | Transaction hash |
| transactionIndex | string | Transaction index in block |
| blockHash | string | Block hash |
| blockNumber | integer | Block number |
| data | string | Event data (hex) |
| logIndex | string | Log index in transaction |
| removed | boolean | Whether log was removed due to chain reorg |
| topics | array | Indexed event arguments (up to 4 topics) |
| decodedTopics | object | Decoded event parameters (when ABI is provided) |
| eventSignature | string | Event signature (e.g., "Transfer(address,address,uint256)") |
| eventName | string | Event name |
