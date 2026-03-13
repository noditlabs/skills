# kaia-klay_getBlockByNumber

> Returns block information for a given block number or tag.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getBlockByNumber

## Supported Chains
kaia (mainnet, kairos)

## Method
`klay_getBlockByNumber`

## Parameters
- **blockNumberOrTag** (`string`): Block number (hex) or tag (`"latest"`, `"earliest"`, `"pending"`).
- **includeTransactions** (`boolean`): If `true`, returns full transaction objects; if `false`, returns only transaction hashes.

## Returns
- **block** (`object|null`): Block object with header fields and optionally full transaction objects, or `null` if not found.
