# base-optimism_rollupconfig

> optimism_rollupConfig

- **Category**: Node API - Base (JSON-RPC)

## Supported Chains

Base (mainnet, sepolia)

## Method

`optimism_rollupConfig`

## Parameters

None - this method takes no parameters.

## Returns

An object containing:
- `genesis` (object): 롤업 제네시스 설정
- `block_time` (integer): L2 creation ( )
- `max_sequencer_drift` (integer): 시퀀서 최대 허용 지연 시간 (초)
- `seq_window_size` (integer): size ( )
- `channel_timeout` (integer): 채널 타임아웃 (블록 수)
- `l1_chain_id` (string): L1 chain ID (hexadecimal)
- `l2_chain_id` (string): L2 chain ID (hexadecimal)
- `batch_inbox_address` (string): L1 contract address
- `deposit_contract_address` (string): L1 contract address
- `l1_system_config_address` (string): L1 contract address

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "optimism_rollupConfig"
}
```
