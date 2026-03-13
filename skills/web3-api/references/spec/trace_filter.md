# trace_filter

> Filters and traces transaction executions matching specified conditions such as block range, sender/receiver addresses, providing targeted trace information.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/trace_filter

## Supported Chains
- Ethereum

## Method
`trace_filter`

## Parameters
An array containing:

1. **Trace Object** (`object`, required): Filter options for tracing.
   - `fromBlock` (`string`, optional): Starting block number as hex string (e.g., `"0x1253B3F"`).
   - `toBlock` (`string`, optional): Ending block number as hex string (e.g., `"0x1253B5F"`).
   - `fromAddress` (`array`, optional): Array of sender addresses to filter by.
   - `toAddress` (`array`, optional): Array of receiver addresses to filter by.
   - `after` (`string`, optional): Trace offset in hex.
   - `count` (`integer`, optional): Number of traces to return.

> **Note**: Wide block ranges or blocks with many events may cause slow responses or timeouts. Keep `fromBlock`-`toBlock` range to 1000 blocks or fewer. Avoid using `"latest"` as a block tag; instead query `eth_blockNumber` first and specify an explicit block number.

## Returns
An array of trace objects, each containing:
- `action` (`object`): Details of the traced action.
  - `callType` (`string`): Type of call (e.g., `"call"`)
  - `from` (`string`): Sender address
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
  "method": "trace_filter",
  "params": [
    {
      "fromBlock": "0x1253B3F",
      "toBlock": "0x1253B5F",
      "fromAddress": ["0xB287eaC48aB21c5FB1d3723830d60b4c797555B0"]
    }
  ]
}
```
