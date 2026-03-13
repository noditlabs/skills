# eth_getUncleByBlockNumberAndIndex

> Returns information about an uncle block by block number and uncle index position.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getUncleByBlockNumberAndIndex

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getUncleByBlockNumberAndIndex`

## Parameters
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `params` | `array` | Yes | Array of 2 items |
| `params[0]` - Block Number or Tag | `string` | Yes | A hex-encoded block number (e.g., `"0x5BAD54"`) or a block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`) |
| `params[1]` - Uncle Index | `string` | Yes | The uncle index position as a hex string (e.g., `"0x0"`) |

## Returns
An uncle block object, or `null` when no uncle was found. The uncle block object contains:
- `difficulty` - Difficulty for this block
- `extraData` - Extra data field of the block
- `gasLimit` - Maximum gas allowed in this block
- `gasUsed` - Total gas used by all transactions in this block
- `hash` - Hash of the uncle block
- `logsBloom` - Bloom filter for the logs of the block
- `miner` - Address of the miner who mined this block
- `mixHash` - Mix hash
- `nonce` - Proof-of-work nonce
- `number` - Block number
- `parentHash` - Hash of the parent block
- `receiptsRoot` - Root of the receipts trie
- `sha3Uncles` - SHA3 of the uncles data
- `size` - Size of this block in bytes
- `stateRoot` - Root of the state trie
- `timestamp` - Unix timestamp of the block
- `transactionsRoot` - Root of the transaction trie
- `uncles` - Array of uncle hashes

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getUncleByBlockNumberAndIndex",
  "params": [
    "0x5BAD54",
    "0x0"
  ]
}
```
