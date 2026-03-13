# eth_createAccessList

> Creates an access list for a transaction per EIP-2930. The access list contains the minimum information needed for transaction execution, reducing network load and gas costs.

- **Category**: Node API (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/eth_createAccessList

## Supported Chains
arbitrum, arc, avalanche, base, bnb, ethereum, giwa, kaia, luniverse, optimism, polygon (common EVM method)

## Method
`eth_createAccessList`

## Parameters
Array of exactly 2 items:

1. **Call Object** (`object`): The transaction call object.
   - `from` (`string`, optional): The sender address.
   - `to` (`string`, required): The contract address to call.
   - `gas` (`string`, optional): Gas limit in hex.
   - `gasPrice` (`string`, optional): Gas price in hex.
   - `value` (`string`, optional): Value to send in hex.
   - `data` (`string`, optional): The encoded method signature and parameters (ABI-encoded).

2. **Block Identifier** (`string`): Block number (hex), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **accessList** (`array`): Array of objects, each containing:
  - `address` (`string`): The contract address accessed.
  - `storageKeys` (`array`): Array of storage slot hex strings accessed.
- **gasUsed** (`string`): The estimated gas used, in hex.

## Example Request
```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "eth_createAccessList",
  "params": [
    {
      "to": "0xdAC17F958D2ee523a2206206994597C13D831ec7",
      "data": "0x70a0823100000000000000000000000047ac0Fb4F2D84898e4D9E7b4DaB3C24507a6D503"
    },
    "latest"
  ]
}
```
