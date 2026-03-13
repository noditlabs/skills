# kaia-kaia_getTransactionReceipt

> Returns the receipt of a transaction by transaction hash.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_getTransactionReceipt

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_getTransactionReceipt`

## Parameters
- **transactionHash** (`string`): 64-char hex transaction hash.

## Returns
- **receipt** (`object|null`): Transaction receipt object containing:
  - `transactionHash`, `transactionIndex`, `blockHash`, `blockNumber`, `from`, `to`, `cumulativeGasUsed`, `gasUsed`, `contractAddress`, `logs`, `logsBloom`, `status`.
