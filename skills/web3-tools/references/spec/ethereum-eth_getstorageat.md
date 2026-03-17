# ethereum-eth_getstorageat

> eth_getStorageAt

- **Category**: Node API - Ethereum (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/ethereum-eth_getstorageat

## Supported Chains

Ethereum (mainnet, sepolia, hoodi)

## Method

`eth_getStorageAt`

## Parameters

Array of parameters:

1. **Address** (`string` (optional)): An Ethereum address (0x-prefixed 40-character hexadecimal string).
2. **Position** (`string` (optional)): The transaction index position as a hexadecimal string.
3. **Block Number or Hash or Tag** (`string` (optional)): A block identifier: block number (hex string, e.g. `"0x1"`), block hash (64-char hex, e.g. `"0x39008..."`), or block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`.

## Returns

- **result** (`string`): hexadecimal string . 0x .

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getStorageAt",
  "params": [
    "0xdac17f958d2ee523a2206206994597c13d831ec7",
    "0x0",
    "latest"
  ]
}
```
