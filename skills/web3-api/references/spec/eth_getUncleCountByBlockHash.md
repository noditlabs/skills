# eth_getUncleCountByBlockHash

> Returns the number of uncles in a block matching the given block hash.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getUncleCountByBlockHash

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getUncleCountByBlockHash`

## Parameters
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `params` | `array` | Yes | Array of 1 item |
| `params[0]` - Block Hash | `string` | Yes | The block hash as a 64-character hex string (e.g., `"0x61a8ad530a8a43e3..."`) |

## Returns
The number of uncle blocks in the given block, encoded as a hex string (e.g., `"0x1"`).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getUncleCountByBlockHash",
  "params": [
    "0x61a8ad530a8a43e3583f8ec163f773ad370329b2375d66433eb82f005e1d6202"
  ]
}
```
