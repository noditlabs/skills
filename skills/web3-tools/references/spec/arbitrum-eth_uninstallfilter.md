# arbitrum-eth_uninstallfilter

> eth_uninstallFilter

- **Category**: Node API - Arbitrum (JSON-RPC)

## Supported Chains

Arbitrum (mainnet, sepolia)

## Method

`eth_uninstallFilter`

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
  "method": "eth_uninstallFilter",
  "params": [
    "0xaf35d60b70eb3b54018456a0d365ea49"
  ]
}
```
