# kaia-kaia_getFilterLogs

> Returns all logs matching a filter created with kaia_newFilter. Equivalent to kaia_getLogs.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_getFilterLogs

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_getFilterLogs`

## Parameters
- **filterId** (`string`): Filter ID returned by a previous newFilter/newBlockFilter/newPendingTransactionFilter call (hex string).

## Returns
- **logs** (`array[object]`): Array of log objects matching the filter.
