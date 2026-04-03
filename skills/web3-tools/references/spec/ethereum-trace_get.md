# ethereum-trace_get

> trace_get

- **Category**: Node API - Ethereum (JSON-RPC)

## Supported Chains

Ethereum (mainnet, sepolia, hoodi)

## Method

`trace_get`

## Parameters

Array of parameters:

1. **Transaction Hash** (`string` (optional)): The transaction hash as a 64-character hexadecimal string.
2. **Trace Index** (`array` (optional)): 

## Returns

An array of objects. execution object . trace_* .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "trace_get",
  "params": [
    "0x17104ac9d3312d8c136b7f44d4b8b47852618065ebfa534bd2d3b5ef218ca1f3",
    [
      "0x0"
    ]
  ]
}
```
