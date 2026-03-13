# getNativeBalanceByAccount

> Retrieve the native token balance held by a specific account. The token type varies by chain.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getNativeBalanceByAccount

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, tron
- Networks: mainnet, sepolia, hoodi, amoy, testnet

## Endpoint
`POST /{chain}/{network}/native/getNativeBalanceByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (e.g., ethereum, tron) |
| network | string | Yes | Target network (e.g., mainnet, sepolia) |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | Yes | Account address to query. EVM: 0x-prefixed 40-char hex. Tron: T-prefixed 34-char base58. |

## Response

### 200 OK

| Field | Type | Description |
|-------|------|-------------|
| ownerAddress | string | Owner address |
| balance | string | Account balance in smallest unit |
