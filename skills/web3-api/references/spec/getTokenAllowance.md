# getTokenAllowance

> Query the amount of tokens approved by an owner for a spender to use via transferFrom.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenAllowance

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

`POST /{chain}/{network}/token/getTokenAllowance`

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
| ownerAddress | string | Yes | Token owner address. |
| spenderAddress | string | Yes | Approved spender address. |

### Tron

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| contractAddress | string | Yes | Contract address (T + 33 base58 chars). |
| ownerAddress | string | Yes | Token owner address (T + 33 base58 chars). |
| spenderAddress | string | Yes | Approved spender address (T + 33 base58 chars). |

## Response

### Success (200)

| Field | Type | Description |
|-------|------|-------------|
| allowance | string | Remaining token amount the spender can use via transferFrom. Changes on `approve` or `transferFrom` calls. |
