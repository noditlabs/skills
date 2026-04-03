# luniverse-eth_getfilterlogs

> eth_getFilterLogs

- **Category**: Node API - Luniverse (JSON-RPC)

## Supported Chains

Luniverse (mainnet)

## Method

`eth_getFilterLogs`

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
  "method": "eth_getFilterLogs",
  "params": [
    "0xaf35d60b70eb3b54018456a0d365ea49"
  ]
}
```
