# arbitrum-eth_getbalance

> eth_getBalance

- **Category**: Node API - Arbitrum (JSON-RPC)

## Supported Chains

Arbitrum (mainnet, sepolia)

## Method

`eth_getBalance`

## Parameters

Array of parameters:

1. **Address** (`string` (optional)): An Ethereum address (0x-prefixed 40-character hexadecimal string).
2. **Block Number or Hash or Tag** (`string` (optional)): A block identifier: block number (hex string, e.g. `"0x1"`), block hash (64-char hex, e.g. `"0x39008..."`), or block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`.

## Returns

- **result** (`string`): An integer encoded as a hexadecimal string (e.g., `'0x1a'`).

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBalance",
  "params": [
    "0xc90d3Ac75D1D36dF0b0a229E73D8409FB7F3c4ab",
    "latest"
  ]
}
```
