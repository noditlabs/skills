# kaia-klay_getLogs

> Returns logs matching filter criteria. Recommend keeping block range under 1000 blocks for performance.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getLogs

## Supported Chains
kaia (mainnet, kairos)

## Method
`klay_getLogs`

## Parameters
- **Log Filter Object** (`object`):
  - `fromBlock` (`string`, optional): Start block (hex number or tag).
  - `toBlock` (`string`, optional): End block (hex number or tag).
  - `address` (`array[string]`, optional): Contract addresses to filter.
  - `topics` (`array[string]`, optional): Topic filters (up to 4), each 32-byte hex.

## Returns
- **logs** (`array[object]`): Array of log objects, each containing:
  - `address`, `topics`, `data`, `blockNumber`, `transactionHash`, `transactionIndex`, `blockHash`, `logIndex`, `removed`.
