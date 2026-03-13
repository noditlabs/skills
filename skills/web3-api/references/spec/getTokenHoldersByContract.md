# getTokenHoldersByContract

> Retrieve the list of holders for a specific token contract, including holder addresses and token balances.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenHoldersByContract

## Supported Chains

| Chain | Networks |
|-------|----------|
| arbitrum | mainnet, sepolia |
| base | mainnet, sepolia |
| bnb | mainnet, testnet |
| chiliz | mainnet, testnet |
| ethereum | mainnet, sepolia, hoodi |
| ethereumclassic | mainnet |
| giwa | mainnet |
| kaia | mainnet, testnet |
| optimism | mainnet, sepolia |
| polygon | mainnet, amoy |
| luniverse | mainnet |
| tron | mainnet, testnet |

## Endpoint

`POST /{chain}/{network}/token/getTokenHoldersByContract`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain. Enum: `arbitrum`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `optimism`, `polygon`, `luniverse`, `tron` |
| network | string | Yes | Target network. Enum: `mainnet`, `sepolia`, `hoodi`, `amoy`, `testnet` |

## Request Body

`Content-Type: application/json`

### EVM Chains

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| contractAddress | string | Yes | Contract address (0x + 40 hex chars). |

### Tron

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| contractAddress | string | Yes | Contract address (T + 33 base58 chars). |

### Pagination (both)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| page | integer | No | Page number (max 100). |
| rpp | integer | No | Results per page (1-1000). |
| cursor | string | No | Cursor for pagination. |
| withCount | boolean | No | Include total count. Default: `false`. |

## Response

### Success (200)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| page | integer | No | Page number. |
| rpp | integer | No | Results per page. |
| cursor | string | No | Cursor for next page. |
| count | integer | No | Total count (only if `withCount=true`). |
| items | array | Yes | List of holder records. |

### Items Schema (EVM)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| ownerAddress | string | Yes | Holder's address (0x + 40 hex). |
| balance | string | Yes | Token balance as decimal string. |
| lastTransferredAt | string | Yes | Last transfer time (ISO 8601). |

### Items Schema (Tron)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| ownerAddress | string | Yes | Holder's Tron address (T + 33 base58). |
| balance | string | Yes | Token balance as decimal string (in SUN for TRX). |
