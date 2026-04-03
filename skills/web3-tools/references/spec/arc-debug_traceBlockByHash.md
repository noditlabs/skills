# arc-debug_traceblockbyhash

> debug_traceBlockByHash

- **Category**: Node API - Arc Debug (JSON-RPC)

## Supported Chains

Arc (testnet)

## Method

`debug_traceBlockByHash`

## Parameters

Array of parameters:

1. **Block Hash** (`string` (optional)): The block hash as a 64-character hexadecimal string.
2. **Trace Option Object** (`object` (optional)): trace object.

   - `tracer` (string): tracer , "callTracer" "prestateTracer" value . 1. `callTracer` : callTracer execution transaction execution result confirmation . transaction , value, , Revert , function . execution (onlyTopCall) call nested call . 2. `prestateTracer`: prestateTracer transaction execution status(pre-state) . transaction execution status code , transaction execution status . prestateTracer status . Enum: `callTracer`, `prestateTracer`.
   - `tracerConfig` (object): tracer Object . Boolean "onlyTopCall" , true main call trace . false sub-call trace.

## Returns

An array of objects. result object . debug_traceTransaction callTracer .

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
