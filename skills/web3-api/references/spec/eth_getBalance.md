# eth_getBalance

> Returns the native token balance of a given account address.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getBalance

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getBalance`

## Parameters
Array of exactly 2 items:

1. **Address** (`string`): The account address to query, as a 40-character hex string (e.g., `"0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045"`).

2. **Block Identifier** (`string`): Block number (hex), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **result** (`string`): The balance in wei as a hexadecimal string (e.g., `"0x8628561832630fc"`).

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getBalance",
  "params": ["0xc90d3Ac75D1D36dF0b0a229E73D8409FB7F3c4ab", "latest"]
}
```
