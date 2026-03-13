# debug_traceBlockByNumber

> Traces all transactions in a block by block number or tag using a specified tracer, providing detailed state changes and call history for debugging.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/debug_traceBlockByNumber

## Supported Chains
- Arbitrum
- Arc
- Avalanche
- Base
- BNB
- Ethereum
- Giwa
- Kaia
- Luniverse
- Optimism
- Polygon

## Method
`debug_traceBlockByNumber`

## Parameters
An array containing:

1. **Block Number or Tag** (`string`, required): The block to trace.
   - Block number as hex string (e.g., `"0x12C1A00"`)
   - Block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`

2. **Trace Option Object** (`object`, optional): Configuration for the tracer.
   - `tracer` (`string`): Tracer type. One of `"callTracer"` or `"prestateTracer"`.
     - `callTracer`: Traces execution path, call stack, return values, gas consumption, and revert reasons.
     - `prestateTracer`: Traces pre-execution state of accounts and contract code.
   - `tracerConfig` (`object`):
     - `onlyTopCall` (`boolean`, default: `true`): When `true`, only traces the main call. When `false`, traces sub-calls as well.

## Returns
An array of trace result objects, each containing:
- `from` (`string`): Sender address
- `gas` (`string`): Gas provided (hex)
- `gasUsed` (`string`): Gas used (hex)
- `to` (`string`): Recipient address
- `input` (`string`): Call input data
- `output` (`string`): Call output data
- `calls` (`array`): Nested sub-calls (when `onlyTopCall` is `false`)
- `value` (`string`): Value transferred (hex)
- `type` (`string`): Call type (e.g., `"CALL"`, `"CALLCODE"`)

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "debug_traceBlockByNumber",
  "params": [
    "latest",
    {
      "tracer": "callTracer",
      "tracerConfig": {
        "onlyTopCall": true
      }
    }
  ]
}
```
