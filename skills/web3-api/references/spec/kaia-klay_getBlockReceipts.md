# kaia-klay_getBlockReceipts

> Returns all transaction receipts for a given block.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getBlockReceipts

## Supported Chains
kaia (mainnet, kairos)

## Method
`klay_getBlockReceipts`

## Parameters
- **Block Identifier** (`string`): Block number (hex, e.g. `"0x1"`), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **receipts** (`array[object]`): Array of transaction receipt objects for all transactions in the block.
