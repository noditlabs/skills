# kaia-kaia_newFilter

> Creates a log filter. Use kaia_getFilterLogs or kaia_getFilterChanges to retrieve results. Recommend block range under 1000.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_newFilter

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_newFilter`

## Parameters
- **Log Filter Object** (`object`):
  - `fromBlock` (`string`, optional): Start block (hex number or tag).
  - `toBlock` (`string`, optional): End block (hex number or tag).
  - `address` (`array[string]`, optional): Contract addresses to filter.
  - `topics` (`array[string]`, optional): Topic filters (up to 4), each 32-byte hex.

## Returns
- **filterId** (`string`): Hex filter ID for use with kaia_getFilterLogs or kaia_getFilterChanges.
