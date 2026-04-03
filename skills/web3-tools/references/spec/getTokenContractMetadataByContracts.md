# getTokenContractMetadataByContracts

> Get Token Contract Metadata by Contracts

- **Category**: Data API - Token

## Supported Chains

- arbitrum
- arc
- base
- bnb
- chiliz
- ethereum
- ethereumclassic
- giwa
- kaia
- luniverse
- optimism
- polygon
- tron

Networks: mainnet, sepolia, testnet, hoodi, kairos, amoy

## Endpoint

`POST /{chain}/{network}/token/getTokenContractMetadataByContracts`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`, `tron`. Default: `arbitrum`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | array | Yes | contract address array parameter . contract address 0x 40 hexadecimal string input . |

## Response

### Success (200) - Successful Response

**Arbitrum (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**Arc (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**Base (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**BNB Smart Chain (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**Chiliz (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**Ethereum (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**Ethereum Classic (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**Giwa (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**Kaia (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**Luniverse (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**Optimism (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**Polygon (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | The contract address field. |
| `deployedTransactionHash` | string | Yes | The hash of the transaction in which the contract was deployed. |
| `deployedAt` | string | Yes | contract deployment field. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address field. |
| `logoUrl` | string | Yes | contract URL field. URL contract . [ ] contract . contract , null . |
| `type` | string | Yes | contract field. contract . (e.g., ERC721, ERC1155, ERC20, ERC721, ERC1155, ERC20) |
| `name` | string | Yes | contract field. , contract creation name input is returned. |
| `symbol` | string | Yes | contract field. , contract creation symbol input is returned. |
| `totalSupply` | string | No | contract field. value token , 10 . contract ERC20 . |
| `decimals` | integer | No | contract field. contract ERC20 ERC1155 . |

**Tron (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `address` | string | Yes | contract address is returned. address contract deployment chain network . |
| `deployedTransactionHash` | string | Yes | contract deployment creation transaction hash value is returned. |
| `deployedAt` | string | Yes | contract deployment is returned. ISO 8601 . |
| `deployerAddress` | string | Yes | contract deployment address is returned. address contract creation network deployment . |
| `logoUrl` | string | Yes | contract URL is returned. URL contract . <strong style='color: red;'>*</strong> contract . |
| `type` | string | Yes | contract is returned. contract . (e.g., TRC20) |
| `name` | string | Yes | contract . , contract creation name input is returned. |
| `symbol` | string | Yes | contract . , contract creation symbol input is returned. |
| `totalSupply` | string | Yes | contract . value token , 10 . |
| `decimals` | integer | Yes | token . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
