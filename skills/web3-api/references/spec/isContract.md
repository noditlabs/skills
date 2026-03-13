# isContract

> Check whether a given address is a smart contract on EVM chains or Tron.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/isContract

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, tron
- Networks: mainnet, testnet, sepolia, hoodi, amoy

## Endpoint
`POST /{chain}/{network}/blockchain/isContract`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| address | string | Yes | Address to check. EVM: 0x-prefixed 40-char hex. Tron: T-prefixed 34-char base58. |

## Response

### 200 OK

| Field | Type | Description |
|-------|------|-------------|
| result | boolean | `true` if the address is a contract, `false` otherwise |
