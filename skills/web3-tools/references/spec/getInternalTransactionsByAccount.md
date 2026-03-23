# getInternalTransactionsByAccount

> Get Internal Transactions By Account

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/getInternalTransactionsByAccount

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

`POST /{chain}/{network}/blockchain/getInternalTransactionsByAccount`

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

### Arbitrum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### Base

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### BNB Smart Chain

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### Chiliz

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### Ethereum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### Ethereum Classic

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### Giwa

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### Kaia

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### Luniverse

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### Optimism

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### Polygon

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withExternalTransaction` | boolean | No | external transaction parameter . external transaction internal transaction , trace index 0 . parameter true input , external transaction . Default: `False`. |

### Tron

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
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

**Tron:**

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
