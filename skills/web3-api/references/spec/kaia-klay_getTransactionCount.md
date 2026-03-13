# kaia-klay_getTransactionCount

> Returns the number of transactions sent from an address (nonce).

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getTransactionCount

## Supported Chains
kaia (mainnet, kairos)

## Method
`klay_getTransactionCount`

## Parameters
- **address** (`string`): 20-byte hex address (e.g. `"0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045"`).
- **Block Identifier** (`string`): Block number (hex, e.g. `"0x1"`), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **count** (`string`): Number of transactions sent as a hex string.
