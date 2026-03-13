# kaia-kaia_getStorageAt

> Returns the value stored at a specific storage slot of a contract address.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_getStorageAt

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_getStorageAt`

## Parameters
- **address** (`string`): 20-byte hex address (e.g. `"0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045"`).
- **position** (`string`): Storage slot index as a hex string.
- **Block Identifier** (`string`): Block number (hex, e.g. `"0x1"`), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **value** (`string`): 32-byte hex value stored at the position.
