# optimism-optimism_rollupConfig

> Query rollup configuration parameters. Returns information including genesis block settings, batch size, sequencer window size, channel timeout, and other rollup configuration options.

- **Category**: Node API - Optimism (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/optimism-optimism_rollupConfig

## Supported Chains
optimism

## Method
`optimism_rollupConfig`

## Parameters
None. This method takes no parameters.

## Returns
`object` - RollupConfig containing rollup configuration fields:
- `genesis` (`object`): Genesis block information including L1 and L2 block references.
- `block_time` (`integer`): The time interval between L2 blocks in seconds.
- `max_sequencer_drift` (`integer`): Maximum time the sequencer can drift from L1.
- `seq_window_size` (`integer`): The sequencer window size in blocks.
- `channel_timeout` (`integer`): The channel timeout in blocks.
- `l1_chain_id` (`integer`): The L1 chain ID.
- `l2_chain_id` (`integer`): The L2 chain ID.
- `batch_inbox_address` (`string`): The batch inbox contract address.
- `deposit_contract_address` (`string`): The deposit contract address.
- `l1_system_config_address` (`string`): The L1 system config contract address.

## Example Request
```json
{
  "jsonrpc": "2.0",
  "id": 1,
  "method": "optimism_rollupConfig",
  "params": []
}
```
