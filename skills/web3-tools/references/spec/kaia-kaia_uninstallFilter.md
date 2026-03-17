# kaia-kaia_uninstallfilter

> kaia_uninstallFilter

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_uninstallfilter

## Supported Chains

Kaia (mainnet, kairos)

## Method

`kaia_uninstallFilter`

## Parameters

Array of parameters:

1. **Filter ID** (`string` (optional)): The filter ID returned by a previous filter creation call.

## Returns

- **result** (`boolean`): value.

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "kaia_uninstallFilter",
  "params": [
    "0xaf35d60b70eb3b54018456a0d365ea49"
  ]
}
```
