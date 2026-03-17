# kaia-klay_getfilterchanges

> klay_getFilterChanges

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getfilterchanges

## Supported Chains

Kaia (mainnet, kairos)

## Method

`klay_getFilterChanges`

## Parameters

Array of parameters:

1. **Filter ID** (`string` (optional)): The filter ID returned by a previous filter creation call.

## Returns

An array of objects. event object . transaction execution event .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "klay_getFilterChanges",
  "params": [
    "0xaf35d60b70eb3b54018456a0d365ea49"
  ]
}
```
