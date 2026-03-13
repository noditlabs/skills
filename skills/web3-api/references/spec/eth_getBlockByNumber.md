# eth_getBlockByNumber

> Returns information about a block identified by its number. When requesting full transactions, response time may increase for blocks with many transactions.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getBlockByNumber

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getBlockByNumber`

## Parameters
Array of exactly 2 items:

1. **Block Number or Tag** (`string`): Block number as a hex string (e.g., `"0x1076B5A"`) or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

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
  "method": "eth_getBlockByNumber",
  "params": ["0x1076B5A", false]
}
```
