# kaia-debug_traceCall

> Executes eth_call in debug mode with tracing, allowing you to trace all stack changes that occur during a simulated call against the current block state.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-debug_traceCall

## Supported Chains
kaia (mainnet, kairos)

## Method
`debug_traceCall`

## Parameters
- **Call Object** (`object`):
  - `from` (`string`, optional): Sender address.
  - `to` (`string`): Target contract address.
  - `gas` (`string`, optional): Gas limit in hex.
  - `gasPrice` (`string`, optional): Gas price in hex.
  - `value` (`string`, optional): Value to send in hex.
  - `data` (`string`, optional): ABI-encoded method call data.
- **Block Identifier** (`string`): Block number (hex, e.g. `"0x1"`), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).
- **Trace Option Object** (`object`):
  - `tracer` (`string`): `"callTracer"` or `"prestateTracer"`.
  - `tracerConfig` (`object`, optional):
    - `onlyTopCall` (`boolean`): If `true`, trace only the top-level call.

## Returns
- **trace** (`object`): Trace result containing call type, from, to, gas, gasUsed, input, output, value, and optionally nested calls.
