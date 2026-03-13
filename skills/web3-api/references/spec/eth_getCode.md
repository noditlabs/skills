# eth_getCode

> Returns the smart contract bytecode at a given address. Returns `0x` if no code exists at the address.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_getCode

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_getCode`

## Parameters
Array of exactly 2 items:

1. **Address** (`string`): The contract address to query, as a 40-character hex string (e.g., `"0xdac17f958d2ee523a2206206994597c13d831ec7"`).

2. **Block Identifier** (`string`): Block number (hex), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **result** (`string`): The bytecode at the given address as a hex string. Returns `"0x"` if no contract exists.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_getCode",
  "params": ["0xdac17f958d2ee523a2206206994597c13d831ec7", "latest"]
}
```
