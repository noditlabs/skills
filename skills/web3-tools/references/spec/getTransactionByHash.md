# getTransactionByHash

> Get Transaction By Hash

- **Category**: Data API - Blockchain

## Supported Chains

- aptos
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
- xrpl

Networks: mainnet, sepolia, testnet, hoodi, kairos, amoy

## Endpoint

`POST /{chain}/{network}/blockchain/getTransactionByHash`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`, `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`, `xrpl`. Default: `aptos`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

### Aptos

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . transaction hash 64 hexadecimal("0x" ) input . |
| `withBalanceChanges` | object | No |  |

### Arbitrum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### Base

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### BNB Smart Chain

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### Chiliz

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### Ethereum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### Ethereum Classic

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### Giwa

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### Kaia

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### Luniverse

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### Optimism

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### Polygon

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash parameter . 0x 64 hexadecimal string input . |
| `withLogs` | boolean | No | logs parameter . parameter true input , . Default: `False`. |
| `withDecode` | boolean | No | decodedInput, decodedLog parameter . parameter true input , . decodedLog logs withDecode true withLogs false decodedLog . decodedInput transaction input result . function function (function selector) , result function . , ERC function . Default: `False`. |

### XRP Ledger

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash input parameter , 64 hexadecimal string . |
| `withBalanceChanges` | boolean | No | balanceChanges parameter . balanceChanges token(XRP) IOU token , true . Default: `False`. |
| `withTokenTransfers` | boolean | No | tokenTransfers parameter . tokenTransfers IOU token , true . Default: `False`. |


## Response

### Success (200) - Successful Response

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
