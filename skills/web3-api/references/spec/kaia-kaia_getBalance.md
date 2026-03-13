# kaia-kaia_getBalance

> Returns the native token (KAIA) balance of an account.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_getBalance

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_getBalance`

## Parameters
- **address** (`string`): 20-byte hex address (e.g. `"0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045"`).
- **Block Identifier** (`string`): Block number (hex, e.g. `"0x1"`), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **balance** (`string`): Account balance in wei as a hex string.
