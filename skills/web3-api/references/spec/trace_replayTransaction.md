# trace_replayTransaction

> Replays a specified transaction locally and traces all events that occurred during execution, without affecting the actual blockchain. Useful for reproducing and analyzing past transaction behavior.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/trace_replayTransaction

## Supported Chains
- Ethereum

## Method
`trace_replayTransaction`

## Parameters
An array containing:

1. **Transaction Hash** (`string`, required): The hash of the transaction to replay. A 64-character hex string prefixed with `0x`.
   - Example: `"0x17104ac9d3312d8c136b7f44d4b8b47852618065ebfa534bd2d3b5ef218ca1f3"`

2. **Trace Type** (`array`, required): One or more trace types to use. Values: `"vmTrace"`, `"trace"`, `"stateDiff"`.
   - `vmTrace`: Detailed step-by-step VM execution including memory state, stack state, and instruction results.
   - `trace`: Step-by-step log of transaction execution including call flow and internal transaction details.
   - `stateDiff`: Differences in account state before and after transaction execution.

## Returns
A result object containing:
- `output` (`string`): Execution output data
- `stateDiff` (`object` or `null`): State differences (if requested)
- `trace` (`array`): Array of trace entries (if requested), each with:
  - `action` (`object`): Call details (from, callType, gas, input, to, value)
  - `result` (`object`): Execution result (gasUsed, output)
  - `subtraces` (`integer`): Number of sub-traces
  - `traceAddress` (`array`): Position in the trace tree
  - `type` (`string`): Trace type
- `vmTrace` (`object` or `null`): VM trace data (if requested)

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "trace_replayTransaction",
  "params": [
    "0x17104ac9d3312d8c136b7f44d4b8b47852618065ebfa534bd2d3b5ef218ca1f3",
    ["trace"]
  ]
}
```
