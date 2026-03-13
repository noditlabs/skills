# eth_chainId

> Returns the chain ID of the network the node is connected to, as a hexadecimal string. The chain ID is defined in EIP-155 and is used in transaction signing to prevent replay attacks.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_chainId

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_chainId`

## Parameters
None - this method takes no parameters.

## Returns
- **result** (`string`): The hexadecimal string representing the chain ID (e.g., `"0x1"` for Ethereum mainnet).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_chainId"
}
```
