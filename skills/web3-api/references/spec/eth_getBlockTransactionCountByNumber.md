# eth_getBlockTransactionCountByNumber

> Returns the number of transactions in a block identified by its block number.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getBlockTransactionCountByNumber

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getBlockTransactionCountByNumber`

## Parameters
Array of exactly 1 item:

1. **Block Number or Tag** (`string`): Block number as a hex string (e.g., `"0x1076B5A"`) or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **result** (`string`): The number of transactions in the block as a hexadecimal string (e.g., `"0x64"` = 100 transactions).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBlockTransactionCountByNumber",
  "params": ["0x1076B5A"]
}
```
