# kaia-eth_getblockreceipts

> eth_getBlockReceipts

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-eth_getblockreceipts

## Supported Chains

Kaia (mainnet, kairos)

## Method

`eth_getBlockReceipts`

## Parameters

Array of parameters:

1. **Block Number or Hash or Tag** (`string` (optional)): A block identifier: block number (hex string, e.g. `"0x1"`), block hash (64-char hex, e.g. `"0x39008..."`), or block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`.

## Returns

An array of objects. transaction object . transaction .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockReceipts",
  "params": [
    "latest"
  ]
}
```
