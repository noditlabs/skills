# eth_gasPrice

> Returns the current estimated gas price of the network in wei.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_gasPrice

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_gasPrice`

## Parameters
None - this method takes no parameters.

## Returns
- **result** (`string`): The current gas price in wei as a hexadecimal string (e.g., `"0x5a44ff4e3"`).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_gasPrice"
}
```
