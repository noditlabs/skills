# web3_clientVersion

> Returns the current client version of the node.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/web3_clientVersion

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`web3_clientVersion`

## Parameters
None. This method takes no parameters.

## Returns
The current client version as a string (e.g., `"erigon/2.57.1/linux-arm64/go1.21.6"`).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "web3_clientVersion"
}
```
