# base-debug_traceBlockByHash

> Traces all transactions in a block by block hash using a specified tracer to debug state changes and call history

- **Category**: Node API - Base (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/base-debug_traceBlockByHash

## Supported Chains
Base (mainnet, sepolia)

## Method
`debug_traceBlockByHash`

## Parameters
| Position | Name | Type | Required | Description |
|----------|------|------|----------|-------------|
| 1 | `blockHash` | `string` | Yes | The block hash to trace. A 64-character hex string prefixed with `0x`. |
| 2 | `traceOption` | `object` | No | Trace configuration object. |

**Trace Option Object:**

| Field | Type | Description |
|-------|------|-------------|
| `tracer` | `string` | Tracer type: `"callTracer"` or `"prestateTracer"`. |
| `tracerConfig` | `object` | Tracer settings. Contains `onlyTopCall` (boolean) - when `true`, traces only the main call; when `false`, includes sub-calls. |

## Returns
An array of trace result objects for each transaction in the block. Each result contains `from`, `to`, `gas`, `gasUsed`, `input`, `output`, `value`, `type`, and optionally `calls` (nested call array).
