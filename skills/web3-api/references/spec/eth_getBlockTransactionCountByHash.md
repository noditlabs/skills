# eth_getBlockTransactionCountByHash

> Returns the number of transactions in a block identified by its hash.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getBlockTransactionCountByHash

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getBlockTransactionCountByHash`

## Parameters
Array of exactly 1 item:

1. **Block Hash** (`string`): The block hash as a 64-character hex string (e.g., `"0x59f63e3840e0f4a1659074c1a4021e881a268a52d31958688da1d66bfbf6d2ca"`).

## Returns
- **result** (`string`): The number of transactions in the block as a hexadecimal string (e.g., `"0x64"` = 100 transactions).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockTransactionCountByHash",
  "params": [
    "0x59f63e3840e0f4a1659074c1a4021e881a268a52d31958688da1d66bfbf6d2ca"
  ]
}
```
