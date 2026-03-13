# eth_getBlockReceipts

> Returns all transaction receipts for a given block. Response time may increase for blocks with many transactions. For individual receipts, use eth_getTransactionReceipt instead.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getBlockReceipts

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getBlockReceipts`

## Parameters
Array of exactly 1 item:

1. **Block Identifier** (`string`): Block number (hex), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
Array of receipt objects, each containing:
- **blockHash** (`string`): Block hash.
- **blockNumber** (`string`): Block number in hex.
- **contractAddress** (`string` | `null`): Contract address created, if any.
- **cumulativeGasUsed** (`string`): Total gas used in the block up to this transaction.
- **effectiveGasPrice** (`string`): Actual gas price paid in hex.
- **from** (`string`): Sender address.
- **gasUsed** (`string`): Gas used by this transaction.
- **logs** (`array`): Array of log objects with `address`, `topics`, `data`, `blockNumber`, `transactionHash`, `transactionIndex`, `blockHash`, `logIndex`, `removed`.
- **logsBloom** (`string`): Bloom filter for logs.
- **status** (`string`): `"0x1"` for success, `"0x0"` for failure.
- **to** (`string`): Recipient address.
- **transactionHash** (`string`): Transaction hash.
- **transactionIndex** (`string`): Transaction index in hex.
- **type** (`string`): Transaction type in hex.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockReceipts",
  "params": ["latest"]
}
```
