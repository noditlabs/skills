# getTransactionsByHashes

> Retrieves information for multiple transactions by their hashes. Supports up to 1000 transactions per request.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getTransactionsByHashes

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, xrpl, aptos
- **Networks**: mainnet, testnet, sepolia, hoodi, amoy

## Endpoint
`POST /{chain}/{network}/blockchain/getTransactionsByHashes`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network |

## Request Body

Schema varies by chain (oneOf). Common fields:

| Name | Type | Required | Description |
|------|------|----------|-------------|
| transactionHashes | array | Yes | Array of transaction hashes (max 1000 items) |
| withLogs | boolean | No | Include event logs (EVM chains) |
| withDecode | boolean | No | Include decoded data (EVM chains) |
| withBalanceChanges | boolean | No | Include balance changes (XRPL, Aptos) |
| withTokenTransfers | boolean | No | Include token transfers (XRPL) |

## Response

Returns an array of transaction objects. Schema varies by chain (EVM, XRPL, Aptos, etc.), each containing chain-specific transaction details.
