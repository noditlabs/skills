# net_version

> Returns the current network ID. Used to identify which Ethereum network the node is connected to.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/net_version

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`net_version`

## Parameters
None. This method takes no parameters.

## Returns
The current network ID as a string. Common network IDs:
- `"1"` - Ethereum Mainnet
- `"3"` - Ropsten Testnet
- `"4"` - Rinkeby Testnet
- `"5"` - Goerli Testnet

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "net_version"
}
```
