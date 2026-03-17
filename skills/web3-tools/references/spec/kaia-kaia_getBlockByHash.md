# kaia-kaia_getblockbyhash

> kaia_getBlockByHash

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_getblockbyhash

## Supported Chains

Kaia (mainnet, kairos)

## Method

`kaia_getBlockByHash`

## Parameters

Array of parameters:

1. **Block Hash** (`string` (optional)): The block hash as a 64-character hexadecimal string.
2. **Include Transactions** (`boolean` (optional)): transaction . true transaction result is returned.

## Returns

An object containing:
- `blockScore` (string): (hexadecimal)
- `extraData` (string): data (hexadecimal)
- `gasUsed` (string): (hexadecimal)
- `governanceData` (string): RLP encoding data (hexadecimal)
- `hash` (string): block hash
- `logsBloom` (string): event Bloom filter (2048 , hexadecimal)
- `number` (string): block number (hexadecimal)
- `parentHash` (string): block hash
- `proposer` (string): node address
- `receiptsRoot` (string): transaction hash

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "kaia_getBlockByHash",
  "params": [
    "0x59f63e3840e0f4a1659074c1a4021e881a268a52d31958688da1d66bfbf6d2ca",
    false
  ]
}
```
