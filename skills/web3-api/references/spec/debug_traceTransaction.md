# debug_traceTransaction

> Replays an already-processed transaction at the node level, providing detailed debugging information including call stack, gas usage, state changes, and log events.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/debug_traceTransaction

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
`debug_traceTransaction`

## Parameters
An array containing:

1. **Transaction Hash** (`string`, required): The hash of the transaction to trace. A 64-character hex string prefixed with `0x`.
   - Example: `"0xda148d856aef6d77d0b76c90ef1091ffe77afe9ee9b1c6cc23f28f042f198bd8"`

2. **Trace Option Object** (`object`, optional): Configuration for the tracer.
   - `tracer` (`string`): Tracer type. One of `"callTracer"` or `"prestateTracer"`.
     - `callTracer`: Traces execution path, call stack, return values, gas consumption, and revert reasons.
     - `prestateTracer`: Traces pre-execution state of accounts and contract code.
   - `tracerConfig` (`object`):
     - `onlyTopCall` (`boolean`, default: `true`): When `true`, only traces the main call. When `false`, traces sub-calls as well.
   - `timeout` (`string`, optional): Override the default 5-second timeout for JavaScript-based tracing. Max `"10s"`. Valid units: `"ns"`, `"us"`, `"ms"`, `"s"` (e.g., `"300ms"`, `"2s45ms"`).

## Returns
A trace result object containing:
- `from` (`string`): Sender address
- `gas` (`string`): Gas provided (hex)
- `gasUsed` (`string`): Gas used (hex)
- `to` (`string`): Recipient address
- `input` (`string`): Call input data
- `value` (`string`): Value transferred (hex)
- `type` (`string`): Call type (e.g., `"CALL"`)

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "debug_traceTransaction",
  "params": [
    "0xda148d856aef6d77d0b76c90ef1091ffe77afe9ee9b1c6cc23f28f042f198bd8",
    {
      "tracer": "callTracer"
    }
  ]
}
```
