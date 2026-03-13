# getNftContractMetadataByContracts

> Retrieve metadata for specific NFT contracts. Supports batch lookup of up to 100 contracts at once.

- **Category**: Data API - NFT
- **Official Docs**: https://developer.nodit.io/reference/getNftContractMetadataByContracts

## Supported Chains

- arbitrum
- base
- bnb
- chiliz
- ethereum
- ethereumclassic
- giwa
- kaia
- optimism
- polygon
- luniverse

## Endpoint

`POST /{chain}/{network}/nft/getNftContractMetadataByContracts`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Target blockchain. Enum: `arbitrum`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `optimism`, `polygon`, `luniverse`. Default: `ethereum` |
| `network` | string | Yes | Target network. Enum: `mainnet`, `sepolia`, `hoodi`, `amoy`, `testnet`. Default: `mainnet` |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo: `nodit-demo` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | string[] | Yes | Array of contract addresses to query. Each address is a 0x-prefixed 40-character hex string. Max 100 addresses. |

## Response

### 200 - Successful Response

Returns an array of contract metadata objects:

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | Contract address |
| `deployedTransactionHash` | string | Yes | Transaction hash of the contract deployment |
| `deployedAt` | string | Yes | Deployment time in ISO 8601 format |
| `deployerAddress` | string | Yes | Address that deployed the contract |
| `logoUrl` | string \| null | Yes | Logo URL for the contract. Null if not available |
| `type` | string | Yes | Contract type (e.g., ERC721, ERC1155) |
| `name` | string | Yes | Contract name. Empty string if not set |
| `symbol` | string | Yes | Contract symbol. Empty string if not set |
| `totalSupply` | string | No | Total supply (ERC20 only) |
| `decimals` | integer | No | Decimal places (ERC20/ERC1155 only) |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
