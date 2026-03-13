# kaia-klay_getTransactionReceipt

> Returns the receipt of a transaction by transaction hash.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-klay_getTransactionReceipt

## Supported Chains
kaia (mainnet, kairos)

## Method
`klay_getTransactionReceipt`

## Parameters
- **transactionHash** (`string`): 64-char hex transaction hash.

## Returns
- **receipt** (`object|null`): Transaction receipt object containing:
  - `transactionHash`, `transactionIndex`, `blockHash`, `blockNumber`, `from`, `to`, `cumulativeGasUsed`, `gasUsed`, `contractAddress`, `logs`, `logsBloom`, `status`.
