# kaia-klay_getCode

> Returns the compiled smart contract bytecode at a given address. Returns `0x` if no code exists.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getCode

## Supported Chains
kaia (mainnet, kairos)

## Method
`klay_getCode`

## Parameters
- **address** (`string`): 20-byte hex address (e.g. `"0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045"`).
- **Block Identifier** (`string`): Block number (hex, e.g. `"0x1"`), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **code** (`string`): Hex-encoded bytecode at the address, or `0x` if none.
