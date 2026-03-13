# debug_traceBlockByHash

> Traces all transactions in a block by block hash using a specified tracer, providing detailed state changes and call history for debugging.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/debug_traceBlockByHash

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
`debug_traceBlockByHash`

## Parameters
An array containing:

1. **Block Hash** (`string`, required): The block hash to trace. A 64-character hex string prefixed with `0x`.
   - Example: `"0x8e38b4dbf6b11fcc3b9dee84fb7986e29ca0a02cecd8977c161ff7333329681e"`

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
  "method": "debug_traceBlockByHash",
  "params": [
    "0x8e38b4dbf6b11fcc3b9dee84fb7986e29ca0a02cecd8977c161ff7333329681e",
    {
      "tracer": "callTracer",
      "tracerConfig": {
        "onlyTopCall": true
      }
    }
  ]
}
```
