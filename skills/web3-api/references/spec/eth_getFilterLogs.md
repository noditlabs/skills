# eth_getFilterLogs

> Returns all logs matching a given filter ID. The filter ID must have been created via eth_newFilter. Returns the same results as eth_getLogs.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getFilterLogs

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getFilterLogs`

## Parameters
Array of exactly 1 item:

1. **Filter ID** (`string`): The filter ID returned by eth_newFilter, as a 32-character hex string (e.g., `"0xaf35d60b70eb3b54018456a0d365ea49"`).

## Returns
Array of log objects, each containing:
- **address** (`string`): Contract address that emitted the log.
- **topics** (`array`): Array of 32-byte topic hex strings.
- **data** (`string`): The log data in hex.
- **blockNumber** (`string`): Block number in hex.
- **transactionHash** (`string`): Transaction hash.
- **transactionIndex** (`string`): Transaction index in hex.
- **blockHash** (`string`): Block hash.
- **logIndex** (`string`): Log index in hex.
- **removed** (`boolean`): `true` if the log was removed due to a chain reorganization.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getFilterLogs",
  "params": ["0xaf35d60b70eb3b54018456a0d365ea49"]
}
```
