# kaia-kaia_getBlockByNumber

> Returns block information for a given block number or tag.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_getBlockByNumber

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_getBlockByNumber`

## Parameters
- **blockNumberOrTag** (`string`): Block number (hex) or tag (`"latest"`, `"earliest"`, `"pending"`).
- **includeTransactions** (`boolean`): If `true`, returns full transaction objects; if `false`, returns only transaction hashes.

## Returns
- **block** (`object|null`): Block object with header fields and optionally full transaction objects, or `null` if not found.
