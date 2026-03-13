# kaia-kaia_createAccessList

> Creates an EIP-2930 access list for a transaction to optimize gas usage.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_createAccessList

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_createAccessList`

## Parameters
- **Call Object** (`object`):
  - `from` (`string`, optional): Sender address.
  - `to` (`string`): Target contract address.
  - `gas` (`string`, optional): Gas limit in hex.
  - `gasPrice` (`string`, optional): Gas price in hex.
  - `value` (`string`, optional): Value to send in hex.
  - `data` (`string`, optional): ABI-encoded method call data.
- **Block Identifier** (`string`): Block number (hex, e.g. `"0x1"`), block hash (64-char hex), or block tag (`"latest"`, `"earliest"`, `"pending"`, `"safe"`, `"finalized"`).

## Returns
- **accessList** (`array`): List of addresses and storage keys the transaction accesses.
- **gasUsed** (`string`): Estimated gas used with the access list.
