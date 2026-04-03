# luniverse-debug_traceblockbynumber

> debug_traceBlockByNumber

- **Category**: Node API - Luniverse Debug (JSON-RPC)

## Supported Chains

Luniverse (mainnet)

## Method

`debug_traceBlockByNumber`

## Parameters

Array of parameters:

1. **Block Number or Tag** (`string` (optional)): . - : hexadecimal string (ex. "0x1") - : enum (ex. "latest", "earliest", "pending") - `earliest`: chain oldest . - `finalized`: finalized , status . (PoS) chain , finalized . - `safe`: network . ' ' network (reorgs) . - `latest`: chain , finalized (reorgs) . latest status . - `pending`: , transaction . transaction status confirmation .
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
  "method": "debug_traceBlockByNumber",
  "params": [
    "latest",
    {
      "tracer": "callTracer",
      "tracerConfig": {
        "onlyTopCall": true
      }
    }
  ]
}
```
