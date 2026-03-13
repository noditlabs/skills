# kaia-klay_getTransactionByBlockHashAndIndex

> Returns transaction information by block hash and transaction index.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getTransactionByBlockHashAndIndex

## Supported Chains
kaia (mainnet, kairos)

## Method
`klay_getTransactionByBlockHashAndIndex`

## Parameters
- **blockHash** (`string`): 64-char hex block hash.
- **transactionIndex** (`string`): Transaction index position in hex.

## Returns
- **transaction** (`object|null`): Transaction object or `null` if not found.
