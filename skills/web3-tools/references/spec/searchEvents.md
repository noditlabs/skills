# searchEvents

> Search Events

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/searchEvents

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

Networks: mainnet, sepolia, testnet, hoodi, kairos, amoy

## Endpoint

`POST /{chain}/{network}/blockchain/searchEvents`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`. Default: `arbitrum`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

### Arbitrum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `eventNames` | array | Yes |  |
| `abi` | string | Yes | contract ABI parameter . JSON ABI input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `eventNames` | array | Yes |  |
| `abi` | string | Yes | contract ABI parameter . JSON ABI input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Base

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `eventNames` | array | Yes |  |
| `abi` | string | Yes | contract ABI parameter . JSON ABI input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### BNB Smart Chain

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `eventNames` | array | Yes |  |
| `abi` | string | Yes | contract ABI parameter . JSON ABI input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Chiliz

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `eventNames` | array | Yes |  |
| `abi` | string | Yes | contract ABI parameter . JSON ABI input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Ethereum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `eventNames` | array | Yes |  |
| `abi` | string | Yes | contract ABI parameter . JSON ABI input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Ethereum Classic

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `eventNames` | array | Yes |  |
| `abi` | string | Yes | contract ABI parameter . JSON ABI input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Giwa

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `eventNames` | array | Yes |  |
| `abi` | string | Yes | contract ABI parameter . JSON ABI input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Kaia

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | object | Yes |  |
| `eventNames` | object | Yes |  |
| `abi` | object | Yes |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . Kaia , "earliest" input Kaia . - Mainnet: 162,900,480 (Aug 29, 2024 11:08:01 UTC+9) - Kairos(Testnet): 156,660,000 (June 13, 2024 10:15:19 UTC+9) |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , Kaia result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . Kaia , "earliest" input Kaia . - Mainnet: 162,900,480 (Aug 29, 2024 11:08:01 UTC+9) - Kairos(Testnet): 156,660,000 (June 13, 2024 10:15:19 UTC+9) |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Luniverse

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `eventNames` | array | Yes |  |
| `abi` | string | Yes | contract ABI parameter . JSON ABI input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Optimism

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `eventNames` | array | Yes |  |
| `abi` | string | Yes | contract ABI parameter . JSON ABI input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Polygon

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `eventNames` | array | Yes |  |
| `abi` | string | Yes | contract ABI parameter . JSON ABI input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |


## Response

### Success (200) - Successful Response

**Arbitrum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Arc:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Base:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**BNB Smart Chain:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Chiliz:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Ethereum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Ethereum Classic:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Giwa:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Kaia:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Luniverse:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Optimism:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Polygon:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
