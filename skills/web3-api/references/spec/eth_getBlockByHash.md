# eth_getBlockByHash

> Returns information about a block identified by its hash. When requesting full transactions, response time may increase for blocks with many transactions.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getBlockByHash

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getBlockByHash`

## Parameters
Array of exactly 2 items:

1. **Block Hash** (`string`): The block hash as a 64-character hex string (e.g., `"0x59f63e3840e0f4a1659074c1a4021e881a268a52d31958688da1d66bfbf6d2ca"`).

2. **Include Transactions** (`boolean`): If `true`, returns full transaction objects; if `false`, returns only transaction hashes.

## Returns
Block object containing:
- **number** (`string`): Block number in hex.
- **hash** (`string`): Block hash.
- **parentHash** (`string`): Parent block hash.
- **nonce** (`string`): Proof-of-work nonce.
- **sha3Uncles** (`string`): SHA3 hash of uncles data.
- **logsBloom** (`string`): Bloom filter for logs.
- **transactionsRoot** (`string`): Root of the transaction trie.
- **stateRoot** (`string`): Root of the state trie.
- **receiptsRoot** (`string`): Root of the receipts trie.
- **miner** (`string`): Address of the block miner/validator.
- **difficulty** (`string`): Difficulty in hex.
- **totalDifficulty** (`string`): Total difficulty in hex.
- **extraData** (`string`): Extra data field.
- **size** (`string`): Block size in bytes (hex).
- **gasLimit** (`string`): Gas limit in hex.
- **gasUsed** (`string`): Gas used in hex.
- **timestamp** (`string`): Unix timestamp in hex.
- **transactions** (`array`): Transaction hashes or full transaction objects.
- **uncles** (`array`): Array of uncle hashes.
- **baseFeePerGas** (`string`): Base fee per gas in hex (post EIP-1559).
- **withdrawals** (`array`): Validator withdrawals (post-Shanghai).
- **withdrawalsRoot** (`string`): Root of withdrawals trie.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockByHash",
  "params": [
    "0x59f63e3840e0f4a1659074c1a4021e881a268a52d31958688da1d66bfbf6d2ca",
    false
  ]
}
```
