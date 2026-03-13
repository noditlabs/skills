# eth_getProof

> Returns the Merkle proof for a given account's storage values. The returned proof can be used to verify that the queried storage state has not been tampered with.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getProof

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getProof`

## Parameters
Array of exactly 3 items:

1. **Address** (`string`): The account address to query, as a 40-character hex string (e.g., `"0xdac17f958d2ee523a2206206994597c13d831ec7"`).

2. **Storage Hashes** (`array` of `string`): Array of storage position hashes to prove, each as a 64-character hex string.

3. **Block Identifier** (`string`): Block number (hex), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **address** (`string`): The account address.
- **accountProof** (`array`): Array of RLP-serialized Merkle-Patricia trie nodes proving the account exists.
- **balance** (`string`): Account balance in hex.
- **codeHash** (`string`): Hash of the account's code.
- **nonce** (`string`): Account nonce in hex.
- **storageHash** (`string`): Hash of the account's storage trie root.
- **storageProof** (`array`): Array of storage proof objects, each containing:
  - `key` (`string`): The storage key.
  - `value` (`string`): The storage value in hex.
  - `proof` (`array`): Array of RLP-serialized Merkle-Patricia trie nodes.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getProof",
  "params": [
    "0xdac17f958d2ee523a2206206994597c13d831ec7",
    ["0x000000000000000000000000c6cde7c39eb2f0f0095f41570af89efc2c1ea828"],
    "latest"
  ]
}
```
