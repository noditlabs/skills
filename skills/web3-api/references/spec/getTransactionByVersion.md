# getTransactionByVersion

> Retrieves detailed information about a specific transaction using its version number (Aptos only).

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getTransactionByVersion

## Supported Chains
- aptos
- **Networks**: mainnet, testnet

## Endpoint
`POST /{chain}/{network}/blockchain/getTransactionByVersion`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (aptos) |
| network | string | Yes | Target network (mainnet, testnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| transactionVersion | integer | Yes | Transaction version number (positive integer) |
| withBalanceChanges | boolean | No | Include balanceChanges field (native APT and token balance changes). May slow response. Default: false |

## Response

| Field | Type | Description |
|-------|------|-------------|
| transactionHash | string | Unique transaction hash (0x + 64 hex) |
| transactionVersion | integer | Sequential transaction ID on chain |
| blockHeight | string | Block height |
| blockTimestamp | string | Block creation timestamp (microseconds UNIX) |
| sender | string | Sender account address |
| success | boolean | Execution success status |
| vmStatus | string | VM execution result status |
| gasUnitPrice | string | Gas unit price in Octas |
| gasUsed | string | Gas consumed |
| maxGasAmount | string | Maximum gas limit |
| sequenceNumber | integer | Sender account sequence number |
| expirationTimestampSecs | integer | Transaction expiration timestamp |
| secondarySigners | array | Multi-sig additional signer addresses |
| events | array | Events emitted during execution |
| balanceInAccounts | array | Accounts that received assets |
| balanceOutAccounts | array | Accounts that sent assets |
| balanceChangedTokens | array | Token types with balance changes |
| balanceChanges | object | Detailed balance change records (optional) |
