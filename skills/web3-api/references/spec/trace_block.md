# trace_block

> Traces the execution of all transactions in a specified block, providing detailed trace information for analyzing transaction processing at the block level.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/trace_block

## Supported Chains
- Ethereum

## Method
`trace_block`

## Parameters
An array containing:

1. **Block Number or Tag** (`string`, required): The block to trace.
   - Block number as hex string (e.g., `"0x12C1A00"`)
   - Block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`

## Returns
An array of trace objects, each containing:
- `action` (`object`): Details of the traced action.
  - `from` (`string`): Sender address
  - `callType` (`string`): Type of call (e.g., `"call"`)
  - `gas` (`string`): Gas provided (hex)
  - `input` (`string`): Call input data
  - `to` (`string`): Recipient address
  - `value` (`string`): Value transferred (hex)
- `blockHash` (`string`): Hash of the block
- `blockNumber` (`integer`): Block number
- `result` (`object`): Execution result.
  - `gasUsed` (`string`): Gas used (hex)
  - `output` (`string`): Output data
- `subtraces` (`integer`): Number of sub-traces
- `traceAddress` (`array`): Position in the trace tree
- `transactionHash` (`string`): Transaction hash
- `transactionPosition` (`integer`): Position in the block
- `type` (`string`): Trace type (e.g., `"call"`)

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "trace_block",
  "params": [
    "latest"
  ]
}
```
