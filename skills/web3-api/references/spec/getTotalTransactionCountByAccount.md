# getTotalTransactionCountByAccount

> Returns the total number of transactions where a specific account address is included as sender or receiver.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getTotalTransactionCountByAccount

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, tron, bitcoin, dogecoin, bitcoincash, xrpl, aptos
- **Networks**: mainnet, sepolia, hoodi, amoy, testnet

## Endpoint
`POST /{chain}/{network}/blockchain/getTotalTransactionCountByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (e.g., ethereum, bitcoin, tron, aptos) |
| network | string | Yes | Target network (e.g., mainnet, sepolia, testnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| accountAddress | string | Yes | Account address to query. Format varies by chain: EVM (0x + 40 hex), Tron (T + 33 base58), Bitcoin (various), XRPL (r + 25-35 base58), Aptos (0x + 64 hex) |

## Response

| Field | Type | Description |
|-------|------|-------------|
| transactionCount | integer | Total number of transactions the account was involved in as sender or receiver |
