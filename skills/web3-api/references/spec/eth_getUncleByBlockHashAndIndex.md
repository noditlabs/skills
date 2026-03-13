# eth_getUncleByBlockHashAndIndex

> Returns information about an uncle block by block hash and uncle index position.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getUncleByBlockHashAndIndex

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getUncleByBlockHashAndIndex`

## Parameters
| Name | Type | Required | Description |
|------|------|----------|-------------|
| `params` | `array` | Yes | Array of 2 items |
| `params[0]` - Block Hash | `string` | Yes | The block hash as a 64-character hex string (e.g., `"0x39008d07edf93c03..."`) |
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
  "method": "eth_getUncleByBlockHashAndIndex",
  "params": [
    "0x59f63e3840e0f4a1659074c1a4021e881a268a52d31958688da1d66bfbf6d2ca",
    "0x0"
  ]
}
```
