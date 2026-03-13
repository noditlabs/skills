# net_listening

> Returns whether the client is actively listening for network connections. Useful as a health check method.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/net_listening

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`net_listening`

## Parameters
None. This method takes no parameters.

## Returns
`true` if the client is actively listening for connections, `false` otherwise.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "net_listening"
}
```
