# giwa-debug_traceCall

> Executes eth_call in debug mode with tracing, tracking all stack changes from a simulated call against a specified block state

- **Category**: Node API - Giwa (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/giwa-debug_traceCall

## Supported Chains
Giwa (mainnet, testnet)

## Method
`debug_traceCall`

## Parameters
| Position | Name | Type | Required | Description |
|----------|------|------|----------|-------------|
| 1 | `callObject` | `object` | Yes | Transaction call object with fields: `from` (string), `to` (string), `gas` (hex string), `gasPrice` (hex string), `value` (hex string), `data` (hex string - method signature hash from ABI). |
| 2 | `blockIdentifier` | `string` | Yes | Block number (hex string), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`). |
| 3 | `traceOption` | `object` | No | Trace configuration object. |

**Trace Option Object:**

| Field | Type | Description |
|-------|------|-------------|
| `tracer` | `string` | Tracer type: `"callTracer"` or `"prestateTracer"`. |
| `tracerConfig` | `object` | Tracer settings. Contains `onlyTopCall` (boolean) - when `true`, traces only the main call; when `false`, includes sub-calls. |

## Returns
A trace result object containing `from`, `to`, `gas`, `gasUsed`, `input`, `output`, `value`, `type`, and optionally `calls` (nested call array).
