# trace_call

> Simulates a transaction call and returns detailed execution information including gas consumption, execution results, and logs, without actually sending the transaction to the blockchain.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/trace_call

## Supported Chains
- Ethereum

## Method
`trace_call`

## Parameters
An array containing:

1. **Call Object** (`object`, required): The transaction call to simulate.
   - `from` (`string`, optional): Sender address.
   - `to` (`string`, required): Target contract address.
   - `gas` (`string`, optional): Gas limit in hex.
   - `gasPrice` (`string`, optional): Gas price in hex.
   - `value` (`string`, optional): Value to send in hex.
   - `data` (`string`, optional): ABI-encoded method signature and parameters.

2. **Trace Type** (`array`, required): One or more trace types to use. Values: `"vmTrace"`, `"trace"`, `"stateDiff"`.
   - `vmTrace`: Detailed step-by-step VM execution including memory state, stack state, and instruction results.
   - `trace`: Step-by-step log of transaction execution including call flow and internal transaction details.
   - `stateDiff`: Differences in account state before and after transaction execution, including storage key changes, balance changes, and contract code changes.

3. **Block Number or Tag** (`string`, required): The block context for the call.
   - Block number as hex string (e.g., `"0x12C1A00"`)
   - Block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`

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
  "method": "trace_call",
  "params": [
    {
      "from": "0xc90d3Ac75D1D36dF0b0a229E73D8409FB7F3c4ab",
      "to": "0xd3CdA913deB6f67967B99D67aCDFa1712C293601",
      "value": "0x186a0"
    },
    ["trace"],
    "latest"
  ]
}
```
