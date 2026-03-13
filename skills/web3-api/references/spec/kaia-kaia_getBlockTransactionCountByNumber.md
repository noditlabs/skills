# kaia-kaia_getBlockTransactionCountByNumber

> Returns the number of transactions in a block identified by block number or tag.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_getBlockTransactionCountByNumber

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_getBlockTransactionCountByNumber`

## Parameters
- **blockNumberOrTag** (`string`): Block number (hex) or tag (`"latest"`, `"earliest"`, `"pending"`).

## Returns
- **count** (`string`): Number of transactions as a hex string.
