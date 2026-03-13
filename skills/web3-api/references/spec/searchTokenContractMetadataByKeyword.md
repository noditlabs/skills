# searchTokenContractMetadataByKeyword

> Search for token contracts by name or symbol keyword. Returns matching contract metadata.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/searchTokenContractMetadataByKeyword

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

`POST /{chain}/{network}/token/searchTokenContractMetadataByKeyword`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain. Enum: `arbitrum`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `optimism`, `polygon`, `luniverse`, `tron` |
| network | string | Yes | Target network. Enum: `mainnet`, `sepolia`, `hoodi`, `amoy`, `testnet` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| keyword | string | Yes | Token name or symbol to search for (e.g., `USDT`). |
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
| items | array | Yes | List of matching contract metadata. |

### Items Schema (EVM)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| address | string | Yes | Contract address. |
| deployedTransactionHash | string | Yes | Deployment transaction hash. |
| deployedAt | string | Yes | Deployment time (ISO 8601). |
| deployerAddress | string | Yes | Deployer address. |
| logoUrl | string | Yes | Logo URL (null if unavailable). |
| type | string | Yes | Contract type (e.g., `ERC20`). |
| name | string | Yes | Contract name. |
| symbol | string | Yes | Contract symbol. |
| totalSupply | string | No | Total supply (ERC20 only). |
| decimals | integer | No | Decimal places (ERC20/ERC1155 only). |

### Items Schema (Tron)

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| address | string | Yes | Contract address. |
| deployedTransactionHash | string | Yes | Deployment transaction hash. |
| deployedAt | string | Yes | Deployment time (ISO 8601). |
| deployerAddress | string | Yes | Deployer address. |
| logoUrl | string | Yes | Logo URL (null if unavailable). |
| type | string | Yes | Contract type (e.g., `TRC20`). |
| name | string | Yes | Contract name. |
| symbol | string | Yes | Contract symbol. |
| totalSupply | string | Yes | Total supply as decimal string. |
| decimals | integer | Yes | Decimal places. |
