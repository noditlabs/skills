# luniverse-eth_getunclecountbyblockhash

> eth_getUncleCountByBlockHash

- **Category**: Node API - Luniverse (JSON-RPC)

## Supported Chains

Luniverse (mainnet)

## Method

`eth_getUncleCountByBlockHash`

## Parameters

Array of parameters:

1. **Block Hash** (`string` (optional)): The block hash as a 64-character hexadecimal string.

## Returns

- **result** (`string`): An integer encoded as a hexadecimal string (e.g., `'0x1a'`).

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getUncleCountByBlockHash",
  "params": [
    "0x61a8ad530a8a43e3583f8ec163f773ad370329b2375d66433eb82f005e1d6202"
  ]
}
```
