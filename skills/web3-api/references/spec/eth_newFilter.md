# eth_newFilter

> Creates a log filter to notify when logs matching given criteria are created. Use with eth_getFilterLogs and eth_uninstallFilter.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_newFilter

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_newFilter`

## Parameters
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `params` | `array` | Yes | Array of 1 log filter object |
| `params[0]` - Log Filter Object | `object` | Yes | Filter criteria object with the following optional fields: |
| `params[0].fromBlock` | `string` | No | A hex-encoded block number or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`) |
| `params[0].toBlock` | `string` | No | A hex-encoded block number or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`) |
| `params[0].address` | `array` | No | Array of contract addresses to filter logs from (20-byte hex strings) |
| `params[0].topics` | `array` | No | Array of 1-4 topic filters. Each topic is a 32-byte hex string used to filter event logs |

> **Note**: Wide block ranges or blocks with many events may cause slow responses or timeouts. Keep `fromBlock` to `toBlock` range within 1000 blocks. Avoid using `latest` as a block tag -- query `eth_blockNumber` first and use the explicit block number.

## Returns
A filter ID as a hex string (e.g., `"0x0100000000000000ee32c7a8d24aac1f"`). This filter ID is used with `eth_getFilterLogs` and `eth_uninstallFilter`.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_newFilter",
  "params": [
    {
      "fromBlock": "latest"
    }
  ]
}
```
