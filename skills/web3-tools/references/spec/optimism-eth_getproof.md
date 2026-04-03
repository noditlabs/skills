# optimism-eth_getproof

> eth_getProof

- **Category**: Node API - Optimism (JSON-RPC)

## Supported Chains

Optimism (mainnet, sepolia)

## Method

`eth_getProof`

## Parameters

Array of parameters:

1. **Address** (`string` (optional)): An Ethereum address (0x-prefixed 40-character hexadecimal string).
2. **Storage Hashes** (`array` (optional)): Storage Hashes address Storage value hashvalue array . hashvalue hashvalue 64 hexadecimal string .
3. **Block Number or Hash or Tag** (`string` (optional)): A block identifier: block number (hex string, e.g. `"0x1"`), block hash (64-char hex, e.g. `"0x39008..."`), or block tag: `"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`.

## Returns

An object containing:
- `address` (string): account address
- `accountProof` (array): status node array (RLP encoding, hexadecimal)
- `balance` (string): balance (hexadecimal, wei )
- `codeHash` (string): code Keccak-256 hash
- `nonce` (string): transaction (hexadecimal)
- `storageHash` (string): hash
- `storageProof` (array): storage key array

## Example Request

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getProof",
  "params": [
    "0xdac17f958d2ee523a2206206994597c13d831ec7",
    [
      "0x000000000000000000000000c6cde7c39eb2f0f0095f41570af89efc2c1ea828"
    ],
    "latest"
  ]
}
```
