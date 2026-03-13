# kaia-debug_traceBlockByHash

> Traces all transactions in a block by block hash using a specified tracer, providing detailed execution information including call stacks, gas usage, and state changes.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-debug_traceBlockByHash

## Supported Chains
kaia (mainnet, kairos)

## Method
`debug_traceBlockByHash`

## Parameters
- **blockHash** (`string`): 64-char hex block hash.
- **Trace Option Object** (`object`):
  - `tracer` (`string`): `"callTracer"` or `"prestateTracer"`.
  - `tracerConfig` (`object`, optional):
    - `onlyTopCall` (`boolean`): If `true`, trace only the top-level call.

## Returns
- **traces** (`array[object]`): Array of trace result objects, one per transaction. Each contains call type, from, to, gas, gasUsed, input, output, value, and optionally nested calls.
