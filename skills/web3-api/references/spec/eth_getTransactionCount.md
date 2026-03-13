# eth_getTransactionCount

> Returns the number of transactions sent from an address (nonce).

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getTransactionCount

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getTransactionCount`

## Parameters
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `params` | `array` | Yes | Array of 2 items |
| `params[0]` - Address | `string` | Yes | The address to query, as a 40-character hex string (e.g., `"0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045"`) |
| `params[1]` - Block Identifier | `string` | Yes | A hex-encoded block number, a 64-character block hash, or a block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`) |

## Returns
The number of transactions sent from the given address, encoded as a hex string (e.g., `"0x2"`).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getTransactionCount",
  "params": [
    "0xc90d3Ac75D1D36dF0b0a229E73D8409FB7F3c4ab",
    "latest"
  ]
}
```
