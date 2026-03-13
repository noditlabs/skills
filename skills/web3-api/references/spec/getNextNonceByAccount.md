# getNextNonceByAccount

> Retrieve the next nonce for a specific account, used for constructing transactions on EVM chains.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getNextNonceByAccount

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse
- Networks: mainnet, testnet, sepolia, hoodi, amoy

## Endpoint
`POST /{chain}/{network}/blockchain/getNextNonceByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | Yes | Account address (0x-prefixed, 40-char hex) |

## Response

### 200 OK

| Field | Type | Description |
|-------|------|-------------|
| nonce | string | Next nonce value (decimal string) |
