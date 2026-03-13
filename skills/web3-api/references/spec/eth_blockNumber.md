# eth_blockNumber

> Returns the number of the most recent block.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_blockNumber

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_blockNumber`

## Parameters
None - this method takes no parameters.

## Returns
- **result** (`string`): The hexadecimal string representing the latest block number (e.g., `"0x1075788"`).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_blockNumber"
}
```
