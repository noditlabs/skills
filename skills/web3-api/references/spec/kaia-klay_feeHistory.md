# kaia-klay_feeHistory

> Returns gas fee history for a range of blocks, useful for setting maxFeePerGas and maxPriorityFeePerGas.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_feeHistory

## Supported Chains
kaia (mainnet, kairos)

## Method
`klay_feeHistory`

## Parameters
- **blockCount** (`integer`): Number of blocks to query (1-1024).
- **newestBlock** (`string`): Block number (hex) or `"latest"`.
- **rewardPercentiles** (`array[integer]`): Percentile values (0-100) in ascending order.

## Returns
- **oldestBlock** (`string`): Oldest block in the range.
- **baseFeePerGas** (`array[string]`): Base fee per gas for each block.
- **gasUsedRatio** (`array[number]`): Gas used ratio for each block.
- **reward** (`array[array[string]]`): Priority fee percentile values per block.
