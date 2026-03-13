# getTokenPricesByContracts

> Retrieve on-chain market prices for tokens by contract address. Supports batch queries of up to 100 contracts. Prices are sourced from CoinMarketCap and may not reflect real-time values.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenPricesByContracts

## Supported Chains

| Chain | Networks |
|-------|----------|
| arbitrum | mainnet |
| base | mainnet |
| bnb | mainnet |
| chiliz | mainnet |
| ethereum | mainnet |
| ethereumclassic | mainnet |
| giwa | mainnet |
| kaia | mainnet |
| optimism | mainnet |
| polygon | mainnet |
| luniverse | mainnet |

## Endpoint

`POST /{chain}/{network}/token/getTokenPricesByContracts`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain. Enum: `arbitrum`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `optimism`, `polygon`, `luniverse` |
| network | string | Yes | Target network. Enum: `mainnet` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| contractAddresses | string[] | Yes | Array of contract addresses (0x + 40 hex chars). Max 100. |
| currency | string | No | Price currency unit. Supports `USD` and `KRW`. Default: `USD`. |

## Response

### Success (200)

Returns an array of price objects.

| Field | Type | Description |
|-------|------|-------------|
| currency | string | Currency code (ISO 4217, e.g., `USD`). |
| price | string | Current token price as decimal string. |
| volumeFor24h | string | 24-hour trading volume. |
| volumeChangeFor24h | string | 24-hour volume change. |
| percentChangeFor1h | string | 1-hour price change percentage. |
| percentChangeFor24h | string | 24-hour price change percentage. |
| percentChangeFor7d | string | 7-day price change percentage. |
| marketCap | string | Market capitalization. |
| updatedAt | string | Last update time (ISO 8601). |
| listings | string[] | List of exchanges where the token is listed. |
| contract | object | Contract metadata (address, name, symbol, type, decimals, totalSupply, etc.). |
