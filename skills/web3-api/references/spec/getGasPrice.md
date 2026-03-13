# getGasPrice

> Retrieve the current gas price for EVM-compatible chains.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getGasPrice

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse
- Networks: mainnet, testnet, sepolia, hoodi, amoy

## Endpoint
`POST /{chain}/{network}/blockchain/getGasPrice`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network |

## Request Body

Empty object `{}` (no parameters required).

## Response

### 200 OK

| Field | Type | Description |
|-------|------|-------------|
| high | string | Highest gas price (decimal string) |
| average | string | Average gas price (decimal string) |
| low | string | Lowest gas price (decimal string) |
| latestBlock | string | Latest block number (decimal string) |
| baseFee | string | Base fee of latest block (decimal string) |
