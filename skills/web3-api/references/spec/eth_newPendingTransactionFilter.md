# eth_newPendingTransactionFilter

> Creates a filter to notify when new pending transactions arrive. Use with eth_getFilterChanges to poll for pending transactions.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_newPendingTransactionFilter

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_newPendingTransactionFilter`

## Parameters
None. This method takes no parameters.

## Returns
A filter ID as a hex string (e.g., `"0x0200000000000000cb91b496c6fee6fb"`). This filter ID is used with `eth_getFilterChanges` to poll for new pending transactions.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_newPendingTransactionFilter"
}
```
