# kaia-klay_getblockbynumber

> klay_getBlockByNumber

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getblockbynumber

## Supported Chains

Kaia (mainnet, kairos)

## Method

`klay_getBlockByNumber`

## Parameters

Array of parameters:

1. **Block Number or Tag** (`string` (optional)): . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation .
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
  "method": "klay_getBlockByNumber",
  "params": [
    "0x1076B5A",
    false
  ]
}
```
