# avalanche-debug_traceTransaction

> Replays an already-processed transaction at the node level, returning detailed execution information including call stack, gas usage, state changes, and log events

- **Category**: Node API - Avalanche (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/avalanche-debug_traceTransaction

## Supported Chains
Avalanche (mainnet, fuji)

## Method
`debug_traceTransaction`

## Parameters
| Position | Name | Type | Required | Description |
|----------|------|------|----------|-------------|
| 1 | `transactionHash` | `string` | Yes | The transaction hash to trace. A 64-character hex string prefixed with `0x`. |
| 2 | `traceOption` | `object` | No | Trace configuration object. |

**Trace Option Object:**

| Field | Type | Description |
|-------|------|-------------|
| `tracer` | `string` | Tracer type: `"callTracer"` or `"prestateTracer"`. |
| `tracerConfig` | `object` | Tracer settings. Contains `onlyTopCall` (boolean) - when `true`, traces only the main call; when `false`, includes sub-calls. |
| `timeout` | `string` | Duration string overriding the default 5s timeout (max `"10s"`). Valid units: `"ns"`, `"us"`, `"ms"`, `"s"`. Example: `"300ms"`, `"2s45ms"`. |

## Returns
A trace result object containing `from`, `to`, `gas`, `gasUsed`, `input`, `output`, `value`, `type`, and optionally `calls` (nested call array).
