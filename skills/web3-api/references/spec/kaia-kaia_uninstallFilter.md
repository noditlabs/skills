# kaia-kaia_uninstallFilter

> Removes a filter by ID. Returns false if the filter was already removed or does not exist.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_uninstallFilter

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_uninstallFilter`

## Parameters
- **filterId** (`string`): Filter ID returned by a previous newFilter/newBlockFilter/newPendingTransactionFilter call (hex string).

## Returns
- **success** (`boolean`): `true` if the filter was successfully removed, `false` otherwise.
