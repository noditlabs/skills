# kaia-debug_traceTransaction

> Replays an already-processed transaction at the node level, returning detailed debugging information including call stacks, gas usage, state changes, and log events.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-debug_traceTransaction

## Supported Chains
kaia (mainnet, kairos)

## Method
`debug_traceTransaction`

## Parameters
- **transactionHash** (`string`): 64-char hex transaction hash.
- **Trace Option Object** (`object`):
  - `tracer` (`string`): `"callTracer"` or `"prestateTracer"`.
  - `tracerConfig` (`object`, optional):
    - `onlyTopCall` (`boolean`): If `true`, trace only the top-level call.
- **timeout** (`string`, optional): Override default 5s timeout (max `"10s"`). Valid units: `ns`, `us`, `ms`, `s`.

## Returns
- **trace** (`object`): Trace result containing call type, from, to, gas, gasUsed, input, output, value, and optionally nested calls.
