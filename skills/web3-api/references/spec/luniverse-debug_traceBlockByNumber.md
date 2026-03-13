# luniverse-debug_traceBlockByNumber

> Traces all transactions in a block by block number or tag using a specified tracer to debug state changes and call history

- **Category**: Node API - Luniverse (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/luniverse-debug_traceBlockByNumber

## Supported Chains
Luniverse (mainnet, testnet)

## Method
`debug_traceBlockByNumber`

## Parameters
| Position | Name | Type | Required | Description |
|----------|------|------|----------|-------------|
| 1 | `blockNumberOrTag` | `string` | Yes | Block number as hex string (e.g., `"0x1076B5A"`) or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`). |
| 2 | `traceOption` | `object` | No | Trace configuration object. |

**Trace Option Object:**

| Field | Type | Description |
|-------|------|-------------|
| `tracer` | `string` | Tracer type: `"callTracer"` or `"prestateTracer"`. |
| `tracerConfig` | `object` | Tracer settings. Contains `onlyTopCall` (boolean) - when `true`, traces only the main call; when `false`, includes sub-calls. |

## Returns
An array of trace result objects for each transaction in the block. Each result contains `from`, `to`, `gas`, `gasUsed`, `input`, `output`, `value`, `type`, and optionally `calls` (nested call array).
