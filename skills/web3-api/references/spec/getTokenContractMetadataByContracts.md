# getTokenContractMetadataByContracts

> Retrieve metadata for specific token contracts. Supports batch queries of up to 100 contracts.

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenContractMetadataByContracts

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

`POST /{chain}/{network}/token/getTokenContractMetadataByContracts`

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
| contractAddresses | string[] | Yes | Array of contract addresses (0x + 40 hex chars). Max 100. |

### Tron

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| contractAddresses | string[] | Yes | Array of contract addresses (T + 33 base58 chars). Max 100. |

## Response

### Success (200)

Returns an array of contract metadata objects.

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| address | string | Yes | Contract address. |
| deployedTransactionHash | string | Yes | Deployment transaction hash. |
| deployedAt | string | Yes | Deployment time (ISO 8601). |
| deployerAddress | string | Yes | Address that deployed the contract. |
| logoUrl | string | Yes | Logo URL (null if unavailable). |
| type | string | Yes | Contract type (e.g., `ERC20`, `ERC721`, `ERC1155`, `TRC20`). |
| name | string | Yes | Contract name (empty string if not set). |
| symbol | string | Yes | Contract symbol (empty string if not set). |
| totalSupply | string | No | Total supply as decimal string (ERC20 only). |
| decimals | integer | No | Decimal places (ERC20/ERC1155 only). |
