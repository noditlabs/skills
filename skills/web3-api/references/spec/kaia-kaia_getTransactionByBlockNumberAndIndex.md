# kaia-kaia_getTransactionByBlockNumberAndIndex

> Returns transaction information by block number and transaction index.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_getTransactionByBlockNumberAndIndex

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_getTransactionByBlockNumberAndIndex`

## Parameters
- **blockNumberOrTag** (`string`): Block number (hex) or tag.
- **transactionIndex** (`string`): Transaction index position in hex.

## Returns
- **transaction** (`object|null`): Transaction object or `null` if not found.
