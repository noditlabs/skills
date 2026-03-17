# polygon-bor_getsignersathash

> bor_getSignersAtHash

- **Category**: Node API - Polygon Bor (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/polygon-bor_getsignersathash

## Supported Chains

Polygon (mainnet, amoy)

## Method

`bor_getSignersAtHash`

## Parameters

Array of parameters:

1. **Block Hash** (`string` (optional)): The block hash as a 64-character hexadecimal string.

## Returns

An array of objects. hexadecimal string array.

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "bor_getSignersAtHash",
  "params": [
    "0xa70c0bff4de8a59f521920deb8b6f3a4885845f2f418409f5fc8daade7717505"
  ]
}
```
