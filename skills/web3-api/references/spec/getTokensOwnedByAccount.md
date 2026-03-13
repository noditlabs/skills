# getTokensOwnedByAccount

> Retrieve the list of tokens owned by a specific account, including token balances and contract metadata. Supports EVM chains, Tron, and Aptos.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokensOwnedByAccount

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
| aptos | mainnet, testnet |

## Endpoint

`POST /{chain}/{network}/token/getTokensOwnedByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain. Enum: `arbitrum`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `optimism`, `polygon`, `luniverse`, `tron`, `aptos` |
| network | string | Yes | Target network. Enum: `mainnet`, `sepolia`, `hoodi`, `amoy`, `testnet` |

## Request Body

`Content-Type: application/json`

### EVM Chains

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | Yes | Account address (0x + 40 hex chars). |
| contractAddresses | string[] | No | Filter by contract addresses. |

### Tron

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | Yes | Account address (T + 33 base58 chars). |
| contractAddresses | string[] | No | Filter by contract addresses. |

### Aptos

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | Yes | Account address (0x + 64 hex chars). |
| assetTypes | string[] | No | Filter by asset types. |
| linkedAssetTypes | string[] | No | Filter by linked asset types (FA object addresses). |

### Pagination (all chains)

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
| items | array | Yes | List of owned token records. |

### Items Schema (EVM)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| ownerAddress | string | Yes | Owner's address. |
| balance | string | Yes | Token balance as decimal string. |
| lastTransferredAt | string | Yes | Last transfer time (ISO 8601). |
| contract | object | No | Contract metadata (address, name, symbol, type, decimals, etc.). |

### Items Schema (Tron)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| ownerAddress | string | Yes | Owner's Tron address. |
| balance | string | Yes | Token balance (in SUN for TRX). |
| contract | object | No | Contract metadata. |

### Items Schema (Aptos)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| ownerAddress | string | Yes | Account address that owns the asset. |
| objectAddress | string | Yes | Object address where asset is stored. |
| value | string | Yes | Asset quantity (raw integer, apply decimals). |
| isFrozen | boolean | Yes | Whether asset transfer is frozen. |
| isPrimary | boolean | Yes | Whether this is the primary object for the owner. |
| assetType | string | Yes | Asset type identifier. |
| tokenStandard | string | Yes | `v1` (Coin) or `v2` (Fungible Asset). |
| linkedAssetType | string | Yes | Common Coin/FA identifier. |
| metadata | object | Yes | Token metadata. |
