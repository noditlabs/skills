# kaia-klay_getFilterChanges

> Polls a filter for changes since the last poll. Works with filters created by kaia_newFilter, kaia_newBlockFilter, or kaia_newPendingTransactionFilter.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getFilterChanges

## Supported Chains
kaia (mainnet, kairos)

## Method
`klay_getFilterChanges`

## Parameters
- **filterId** (`string`): Filter ID returned by a previous newFilter/newBlockFilter/newPendingTransactionFilter call (hex string).

## Returns
- **changes** (`array`): Array of log objects, block hashes, or transaction hashes depending on filter type.
