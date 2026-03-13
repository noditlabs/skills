# kaia-debug_traceBlockByNumber

> Traces all transactions in a block by block number using a specified tracer, providing detailed execution information including call stacks, gas usage, and state changes.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-debug_traceBlockByNumber

## Supported Chains
kaia (mainnet, kairos)

## Method
`debug_traceBlockByNumber`

## Parameters
- **blockNumberOrTag** (`string`): Block number (hex) or tag (`"latest"`, `"earliest"`, `"pending"`).
- **Trace Option Object** (`object`):
  - `tracer` (`string`): `"callTracer"` or `"prestateTracer"`.
  - `tracerConfig` (`object`, optional):
    - `onlyTopCall` (`boolean`): If `true`, trace only the top-level call.

## Returns
- **traces** (`array[object]`): Array of trace result objects, one per transaction. Each contains call type, from, to, gas, gasUsed, input, output, value, and optionally nested calls.
