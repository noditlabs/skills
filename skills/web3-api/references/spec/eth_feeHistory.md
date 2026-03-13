# eth_feeHistory

> Returns gas fee history for a requested block range. Use this to determine appropriate values for maxFeePerGas and maxPriorityFeePerGas when creating transactions.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_feeHistory

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_feeHistory`

## Parameters
Array of exactly 3 items:

1. **Block Count** (`integer`): Number of blocks to query (1-1024). Fewer may be returned if not all blocks are available.

2. **Newest Block** (`string`): The newest block to query. Block number (hex string) or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

3. **Reward Percentiles** (`array` of `integer`): Percentile values (0-100) in ascending order to sample priority fees, weighted by gas used per block.

## Returns
- **oldestBlock** (`string`): Hex block number of the oldest block in the range.
- **reward** (`array`): Array of arrays containing effective priority fee per gas at the requested percentiles for each block.
- **baseFeePerGas** (`array`): Array of base fees per gas (hex) for each block (includes one extra entry for the next block).
- **gasUsedRatio** (`array`): Array of gas used ratios (float) for each block.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_feeHistory",
  "params": [2, "latest", [0, 100]]
}
```
