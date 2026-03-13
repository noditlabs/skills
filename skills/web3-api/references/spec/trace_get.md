# trace_get

> Retrieves a specific trace from a transaction by its index, providing information about function calls, gas consumption, and generated logs during execution.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/trace_get

## Supported Chains
- Ethereum

## Method
`trace_get`

## Parameters
An array containing:

1. **Transaction Hash** (`string`, required): The hash of the transaction to trace. A 64-character hex string prefixed with `0x`.
   - Example: `"0x17104ac9d3312d8c136b7f44d4b8b47852618065ebfa534bd2d3b5ef218ca1f3"`

2. **Trace Index** (`array`, required): Array of trace indices to retrieve, each as a hex string.
   - Example: `["0x0"]`

## Returns
A trace object containing:
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
  "method": "trace_get",
  "params": [
    "0x17104ac9d3312d8c136b7f44d4b8b47852618065ebfa534bd2d3b5ef218ca1f3",
    ["0x0"]
  ]
}
```
