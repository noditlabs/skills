# ethereum-trace_transaction

> trace_transaction

- **Category**: Node API - Ethereum (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/ethereum-trace_transaction

## Supported Chains

Ethereum (mainnet, sepolia, hoodi)

## Method

`trace_transaction`

## Parameters

Array of parameters:

1. **Transaction Hash** (`string` (optional)): The transaction hash as a 64-character hexadecimal string.

## Returns

An array of objects. execution object . trace_* .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "trace_transaction",
  "params": [
    "0x17104ac9d3312d8c136b7f44d4b8b47852618065ebfa534bd2d3b5ef218ca1f3"
  ]
}
```
