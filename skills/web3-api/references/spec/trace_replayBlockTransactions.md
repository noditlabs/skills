# trace_replayBlockTransactions

> Replays all transactions in a specified block and traces their execution, providing detailed trace information for block-level transaction analysis.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/trace_replayBlockTransactions

## Supported Chains
- Ethereum

## Method
`trace_replayBlockTransactions`

## Parameters
An array containing:

1. **Block Number or Tag** (`string`, required): The block to replay.
   - Block number as hex string (e.g., `"0x12C1A00"`)
   - Block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`

2. **Trace Type** (`array`, required): One or more trace types to use. Values: `"vmTrace"`, `"trace"`, `"stateDiff"`.
   - `vmTrace`: Detailed step-by-step VM execution including memory state, stack state, and instruction results.
   - `trace`: Step-by-step log of transaction execution including call flow and internal transaction details.
   - `stateDiff`: Differences in account state before and after transaction execution.

## Returns
An array of replay results, each containing:
- `output` (`string`): Execution output data
- `stateDiff` (`object` or `null`): State differences (if requested)
- `trace` (`array`): Array of trace entries (if requested), each with:
  - `action` (`object`): Call details (from, callType, gas, input, to, value)
  - `result` (`object`): Execution result (gasUsed, output)
  - `subtraces` (`integer`): Number of sub-traces
  - `traceAddress` (`array`): Position in the trace tree
  - `type` (`string`): Trace type
- `vmTrace` (`object` or `null`): VM trace data (if requested)
- `transactionHash` (`string`): Transaction hash

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "trace_replayBlockTransactions",
  "params": [
    "latest",
    ["trace"]
  ]
}
```
