# kaia-klay_getBlockByHash

> Returns block information for a given block hash.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getBlockByHash

## Supported Chains
kaia (mainnet, kairos)

## Method
`klay_getBlockByHash`

## Parameters
- **blockHash** (`string`): 64-char hex block hash.
- **includeTransactions** (`boolean`): If `true`, returns full transaction objects; if `false`, returns only transaction hashes.

## Returns
- **block** (`object|null`): Block object with header fields and optionally full transaction objects, or `null` if not found.
