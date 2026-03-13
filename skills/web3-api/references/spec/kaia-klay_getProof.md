# kaia-klay_getProof

> Returns merkle-proof for an account's storage values, allowing verification that storage data has not been tampered with.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getProof

## Supported Chains
kaia (mainnet, kairos)

## Method
`klay_getProof`

## Parameters
- **address** (`string`): 20-byte hex address (e.g. `"0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045"`).
- **storageKeys** (`array[string]`): Array of 64-char hex storage position hashes.
- **Block Identifier** (`string`): Block number (hex, e.g. `"0x1"`), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **accountProof** (`array[string]`): Merkle proof nodes for the account.
- **balance** (`string`): Account balance.
- **codeHash** (`string`): Hash of the account code.
- **nonce** (`string`): Account nonce.
- **storageHash** (`string`): Storage root hash.
- **storageProof** (`array[object]`): Proof for each requested storage key.
