# eth_getUncleCountByBlockNumber

> Returns the number of uncles in a block matching the given block number.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getUncleCountByBlockNumber

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getUncleCountByBlockNumber`

## Parameters
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `params` | `array` | Yes | Array of 1 item |
| `params[0]` - Block Number or Tag | `string` | Yes | A hex-encoded block number (e.g., `"0x5BAD54"`) or a block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`) |

## Returns
The number of uncle blocks in the given block, encoded as a hex string (e.g., `"0x1"`).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getUncleCountByBlockNumber",
  "params": [
    "0x5BAD54"
  ]
}
```
