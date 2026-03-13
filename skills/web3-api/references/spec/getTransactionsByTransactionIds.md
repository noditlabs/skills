# getTransactionsByTransactionIds

> Retrieves information for multiple transactions by their IDs (UTXO chains). Supports up to 1000 transactions per request.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getTransactionsByTransactionIds

## Supported Chains
- bitcoin, dogecoin, bitcoincash
- **Networks**: mainnet, testnet

## Endpoint
`POST /{chain}/{network}/blockchain/getTransactionsByTransactionIds`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (bitcoin, dogecoin, bitcoincash) |
| network | string | Yes | Target network (mainnet, testnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| transactionIds | array | Yes | Array of transaction IDs (64-char hex without 0x, max 1000 items, min 1) |

## Response

Returns an array of UTXO transaction objects containing id, hash, version, lockTime, size, vsize, weight, fee, vinCount, voutCount, blockHeight, blockHash, blockTimestamp, vin (inputs), and vout (outputs).
