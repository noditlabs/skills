# getTransactionsByAccount

> Retrieves a paginated list of transactions associated with a specific account address.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getTransactionsByAccount

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, tron, bitcoin, dogecoin, bitcoincash, xrpl, aptos
- **Networks**: mainnet, testnet, sepolia, hoodi, amoy

## Endpoint
`POST /{chain}/{network}/blockchain/getTransactionsByAccount`

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
| accountAddress | string | Yes | Account address (format varies by chain) |
| fromBlock | string | No | Start block (number, hash, or tag) |
| toBlock | string | No | End block (number, hash, or tag). Default: latest |
| fromDate | string | No | Start date (ISO 8601). Cannot be used with fromBlock/toBlock |
| toDate | string | No | End date (ISO 8601). Cannot be used with fromBlock/toBlock |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (max 1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count. Default: false |

## Response

| Field | Type | Description |
|-------|------|-------------|
| page | integer | Current page number |
| rpp | integer | Results per page |
| cursor | string | Next page cursor |
| count | integer | Total count (if withCount=true) |
| items | array | List of transaction objects (schema varies by chain) |
