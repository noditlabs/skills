# getBlocksWithinRange

> Retrieve a list of blocks within a specified time period or block range.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getBlocksWithinRange

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, aptos
- Networks: mainnet, testnet, sepolia, hoodi, amoy

## Endpoint
`POST /{chain}/{network}/blockchain/getBlocksWithinRange`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| fromBlock | string | No | Start block (number, hash with 0x prefix, or tag: earliest/latest) |
| toBlock | string | No | End block (number, hash with 0x prefix, or tag: earliest/latest) |
| fromDate | string | No | Start date (ISO 8601). Cannot be used with fromBlock/toBlock. |
| toDate | string | No | End date (ISO 8601). Cannot be used with fromBlock/toBlock. |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (1-1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count (default: false) |

## Response

### 200 OK (Paginated)

Paginated response with `page`, `rpp`, `cursor`, `count`, and `items` array.

Items follow the same schema as `getBlockByHashOrNumber` response (EVM or Aptos format depending on chain).
