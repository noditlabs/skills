# giwa-debug_tracecall

> debug_traceCall

- **Category**: Node API - Giwa Debug (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/giwa-debug_tracecall

## Supported Chains

Giwa (sepolia)

## Method

`debug_traceCall`

## Parameters

Array of parameters:

1. **Call Object** (`object` (optional)): The transaction call object.

   - `from` (string): transaction from address input.
   - `to` (string): transaction to address input.
   - `gas` (string): transaction hex input . contract call 0x0 input .
   - `gasPrice` (string): hex input.
   - `value` (string): transaction value value.
   - `data` (string): execution transaction method signature hashvalue . ABI .
2. **Block Number or Hash or Tag** (`string` (optional)): A block identifier: block number (hex string, e.g. `"0x1"`), block hash (64-char hex, e.g. `"0x39008..."`), or block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`.
3. **Trace Option Object** (`object` (optional)): trace object.

   - `tracer` (string): tracer , "callTracer" "prestateTracer" value . 1. `callTracer` : callTracer execution transaction execution result confirmation . transaction , value, , Revert , function . execution (onlyTopCall) call nested call . 2. `prestateTracer`: prestateTracer transaction execution status(pre-state) . transaction execution status code , transaction execution status . prestateTracer status . Enum: `callTracer`, `prestateTracer`.
   - `tracerConfig` (object): tracer Object . Boolean "onlyTopCall" , true main call trace . false sub-call trace.

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
  "method": "debug_traceCall",
  "params": [
    {
      "from": "0xc90d3Ac75D1D36dF0b0a229E73D8409FB7F3c4ab",
      "to": "0xd3CdA913deB6f67967B99D67aCDFa1712C293601",
      "value": "0x186a0"
    },
    "finalized",
    {
      "tracer": "callTracer"
    }
  ]
}
```
