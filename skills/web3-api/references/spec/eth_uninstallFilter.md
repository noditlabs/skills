# eth_uninstallFilter

> Uninstalls a filter by its ID. Should be called when a filter is no longer needed.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_uninstallFilter

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_uninstallFilter`

## Parameters
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `params` | `array` | Yes | Array of 1 item |
| `params[0]` - Filter ID | `string` | Yes | The filter ID previously created via `eth_newFilter`, `eth_newBlockFilter`, or `eth_newPendingTransactionFilter`. A 32-character hex string (e.g., `"0xaf35d60b70eb3b54018456a0d365ea49"`) |

## Returns
`true` if the filter was successfully uninstalled, `false` if the filter was already removed or does not exist.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_uninstallFilter",
  "params": [
    "0xaf35d60b70eb3b54018456a0d365ea49"
  ]
}
```
