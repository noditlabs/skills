# polygon-debug_tracetransaction

> debug_traceTransaction

- **Category**: Node API - Polygon Debug (JSON-RPC)

## Supported Chains

Polygon (mainnet, amoy)

## Method

`debug_traceTransaction`

## Parameters

Array of parameters:

1. **Transaction Hash** (`string` (optional)): The transaction hash as a 64-character hexadecimal string.
2. **Trace Option Object** (`object` (optional)): trace object.

   - `tracer` (string): tracer , "callTracer" "prestateTracer" value . 1. `callTracer` : callTracer execution transaction execution result confirmation . transaction , value, , Revert , function . execution (onlyTopCall) call nested call . 2. `prestateTracer`: prestateTracer transaction execution status(pre-state) . transaction execution status code , transaction execution status . prestateTracer status . Enum: `callTracer`, `prestateTracer`.
   - `tracerConfig` (object): tracer Object . Boolean "onlyTopCall" , true main call trace . false sub-call trace.
   - `timeout` (string): JavaScript 5 . "10s" . "ns", "us", "ms", "s" , "300ms" "2s45ms" .

## Returns

An object containing:
- `from` (string): sender address
- `gas` (string): gas limit (hexadecimal)
- `gasUsed` (string): (hexadecimal)
- `to` (string): recipient address
- `input` (string): input data (hexadecimal)
- `output` (string): data (hexadecimal)
- `value` (string): ETH (hexadecimal, wei )
- `type` (string): (CALL, CREATE, STATICCALL )
- `calls` (array): (sub-call)
- `error` (string): execution ( )

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "debug_traceTransaction",
  "params": [
    "0xda148d856aef6d77d0b76c90ef1091ffe77afe9ee9b1c6cc23f28f042f198bd8",
    {
      "tracer": "callTracer"
    }
  ]
}
```
