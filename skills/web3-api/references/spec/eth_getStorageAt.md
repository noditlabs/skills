# eth_getStorageAt

> Returns the value stored at a specific storage slot for a given address.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getStorageAt

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getStorageAt`

## Parameters
Array of exactly 3 items:

1. **Address** (`string`): The contract address to query, as a 40-character hex string (e.g., `"0xdac17f958d2ee523a2206206994597c13d831ec7"`).

2. **Position** (`string`): The storage slot index as a hex string (e.g., `"0x0"`).

3. **Block Identifier** (`string`): Block number (hex), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **result** (`string`): The value at the storage position as a 32-byte hex string (e.g., `"0x000000000000000000000000c6cde7c39eb2f0f0095f41570af89efc2c1ea828"`).

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
