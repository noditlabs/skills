# debug_traceCall

> Executes eth_call in debug mode with tracing, allowing you to track all stack changes when performing a specific call based on the current block state.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/debug_traceCall

## Supported Chains
- Arbitrum
- Arc
- Avalanche
- Base
- BNB
- Ethereum
- Giwa
- Kaia
- Luniverse
- Optimism
- Polygon

## Method
`debug_traceCall`

## Parameters
An array containing:

1. **Call Object** (`object`, required): The transaction call to simulate.
   - `from` (`string`, optional): Sender address.
   - `to` (`string`, required): Target contract address.
   - `gas` (`string`, optional): Gas limit in hex.
   - `gasPrice` (`string`, optional): Gas price in hex.
   - `value` (`string`, optional): Value to send in hex.
   - `data` (`string`, optional): ABI-encoded method signature and parameters.

2. **Block Identifier** (`string`, required): The block context for the call.
   - Block number as hex string (e.g., `"0x12C1A00"`)
   - Block hash as 64-character hex string
   - Block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`

3. **Trace Option Object** (`object`, optional): Configuration for the tracer.
   - `tracer` (`string`): Tracer type. One of `"callTracer"` or `"prestateTracer"`.
   - `tracerConfig` (`object`):
     - `onlyTopCall` (`boolean`, default: `true`): When `true`, only traces the main call.

## Returns
A trace result object containing:
- `from` (`string`): Sender address
- `gas` (`string`): Gas provided (hex)
- `gasUsed` (`string`): Gas used (hex)
- `to` (`string`): Recipient address
- `input` (`string`): Call input data
- `output` (`string`): Call output data
- `value` (`string`): Value transferred (hex)
- `type` (`string`): Call type (e.g., `"CALL"`)

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
