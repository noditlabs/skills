# eth_maxPriorityFeePerGas

> Returns the current max priority fee per gas in wei, used for EIP-1559 transactions.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_maxPriorityFeePerGas

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_maxPriorityFeePerGas`

## Parameters
None. This method takes no parameters.

## Returns
The current max priority fee per gas in wei, encoded as a hex string (e.g., `"0x989680"`).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_maxPriorityFeePerGas"
}
```
