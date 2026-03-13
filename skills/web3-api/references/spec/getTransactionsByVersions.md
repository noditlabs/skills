# getTransactionsByVersions

> Retrieves information for multiple transactions by their version numbers (Aptos only). Supports up to 1000 transactions per request.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getTransactionsByVersions

## Supported Chains
- aptos
- **Networks**: mainnet, testnet

## Endpoint
`POST /{chain}/{network}/blockchain/getTransactionsByVersions`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (aptos) |
| network | string | Yes | Target network (mainnet, testnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| transactionVersions | array | Yes | Array of transaction versions (positive integers, max 1000 items, min 1) |
| withBalanceChanges | boolean | No | Include balanceChanges field (native APT and token balance changes). May slow response. Default: false |

## Response

Returns an array of Aptos transaction objects containing transactionHash, transactionVersion, blockHeight, blockTimestamp, sender, success, vmStatus, gasUnitPrice, gasUsed, maxGasAmount, sequenceNumber, expirationTimestampSecs, secondarySigners, events, balanceInAccounts, balanceOutAccounts, balanceChangedTokens, and optionally balanceChanges.
