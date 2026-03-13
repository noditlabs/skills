# kaia-kaia_sendRawTransaction

> Submits a signed transaction to the network. The transaction must be signed client-side with a private key.

- **Category**: Node API - Kaia (JSON-RPC)
- **Official Docs**: https://developer.nodit.io/reference/kaia-kaia_sendRawTransaction

## Supported Chains
kaia (mainnet, kairos)

## Method
`kaia_sendRawTransaction`

## Parameters
- **signedTransactionData** (`string`): RLP-encoded signed transaction data as a hex string.

## Returns
- **transactionHash** (`string`): 64-char hex hash of the submitted transaction.
