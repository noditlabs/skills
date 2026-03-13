# giwa-optimism_rollupConfig

> Retrieves the rollup configuration parameters including genesis block info, batch size, sequencer window size, channel timeout, and other operational settings

- **Category**: Node API - Giwa (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/giwa-optimism_rollupConfig

## Supported Chains
Giwa (mainnet, testnet)

## Method
`optimism_rollupConfig`

## Parameters
This method takes no parameters.

## Returns
A rollup configuration object containing:

| Field | Type | Description |
|-------|------|-------------|
| `genesis` | `object` | Genesis block info with `l1` (hash, number), `l2` (hash, number), `l2_time`, and `system_config` (batcherAddr, overhead, scalar, gasLimit). |
| `block_time` | `integer` | Block time in seconds. |
| `max_sequencer_drift` | `integer` | Maximum sequencer drift in seconds. |
| `seq_window_size` | `integer` | Sequencer window size. |
| `channel_timeout` | `integer` | Channel timeout value. |
| `l1_chain_id` | `integer` | L1 chain ID. |
| `l2_chain_id` | `integer` | L2 chain ID. |
| `batch_inbox_address` | `string` | Batch inbox contract address. |
| `deposit_contract_address` | `string` | Deposit contract address. |
| `l1_system_config_address` | `string` | L1 system config contract address. |
| `protocol_versions_address` | `string` | Protocol versions contract address. |
