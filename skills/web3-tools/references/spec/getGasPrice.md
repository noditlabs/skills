# getGasPrice

> Get Gas Price

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/getGasPrice

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

`POST /{chain}/{network}/blockchain/getGasPrice`

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


## Response

### Success (200) - Successful Response

**Arbitrum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

**Arc:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

**Base:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

**BNB Smart Chain:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

**Chiliz:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

**Ethereum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

**Ethereum Classic:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

**Giwa:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

**Kaia:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

**Luniverse:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

**Optimism:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

**Polygon:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `high` | string | Yes | Gas Price field. 10 . |
| `average` | string | Yes | Gas Price field. 10 . |
| `low` | string | Yes | Gas Price field. 10 . |
| `latestBlock` | string | Yes | latest block field. 10 . |
| `baseFee` | string | Yes | latest block fee field. 10 . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
