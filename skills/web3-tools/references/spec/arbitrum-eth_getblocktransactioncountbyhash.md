# arbitrum-eth_getblocktransactioncountbyhash

> eth_getBlockTransactionCountByHash

- **Category**: Node API - Arbitrum (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/arbitrum-eth_getblocktransactioncountbyhash

## Supported Chains

Arbitrum (mainnet, sepolia)

## Method

`eth_getBlockTransactionCountByHash`

## Parameters

Array of parameters:

1. **Block Hash** (`string` (optional)): The block hash as a 64-character hexadecimal string.

## Returns

- **result** (`string`): An integer encoded as a hexadecimal string (e.g., `'0x1a'`).

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
