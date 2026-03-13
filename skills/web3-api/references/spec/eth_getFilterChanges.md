# eth_getFilterChanges

> Returns filter results for a given filter ID. The filter ID must have been created via eth_newFilter, eth_newBlockFilter, or eth_newPendingTransactionFilter.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getFilterChanges

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getFilterChanges`

## Parameters
Array of exactly 1 item:

1. **Filter ID** (`string`): The filter ID returned when creating the filter, as a 32-character hex string (e.g., `"0xaf35d60b70eb3b54018456a0d365ea49"`).

## Returns
Array of log objects (for log filters), each containing:
- **address** (`string`): Contract address that emitted the log.
- **topics** (`array`): Array of 32-byte topic hex strings.
- **data** (`string`): The log data in hex.
- **blockNumber** (`string`): Block number in hex.
- **transactionHash** (`string`): Transaction hash.
- **transactionIndex** (`string`): Transaction index in hex.
- **blockHash** (`string`): Block hash.
- **logIndex** (`string`): Log index in hex.
- **removed** (`boolean`): `true` if the log was removed due to a chain reorganization.

For block filters, returns an array of block hashes. For pending transaction filters, returns an array of transaction hashes.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getFilterChanges",
  "params": ["0xaf35d60b70eb3b54018456a0d365ea49"]
}
```
