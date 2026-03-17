# optimism-eth_getcode

> eth_getCode

- **Category**: Node API - Optimism (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/optimism-eth_getcode

## Supported Chains

Optimism (mainnet, sepolia)

## Method

`eth_getCode`

## Parameters

Array of parameters:

1. **Address** (`string` (optional)): An Ethereum address (0x-prefixed 40-character hexadecimal string).
2. **Block Number or Hash or Tag** (`string` (optional)): A block identifier: block number (hex string, e.g. `"0x1"`), block hash (64-char hex, e.g. `"0x39008..."`), or block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`.

## Returns

- **result** (`string`): hexadecimal string . 0x .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getCode",
  "params": [
    "0xdac17f958d2ee523a2206206994597c13d831ec7",
    "latest"
  ]
}
```
