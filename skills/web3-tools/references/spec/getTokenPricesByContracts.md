# getTokenPricesByContracts

> Get Token Prices by Contracts

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenPricesByContracts

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

`POST /{chain}/{network}/token/getTokenPricesByContracts`

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
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |

### Base

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |

### BNB Smart Chain

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |

### Chiliz

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |

### Ethereum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |

### Ethereum Classic

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |

### Giwa

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |

### Kaia

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |

### Luniverse

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |

### Optimism

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |

### Polygon

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contractAddresses` | object | Yes |  |
| `currency` | string | No | Token Price parameter . USD KRW . value USD . Default: `USD`. |


## Response

### Success (200) - Successful Response

**Arbitrum (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

**Arc (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

**Base (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

**BNB Smart Chain (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

**Chiliz (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

**Ethereum (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

**Ethereum Classic (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

**Giwa (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

**Kaia (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

**Luniverse (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

**Optimism (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

**Polygon (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `currency` | string | No | . ISO 4217 code . |
| `price` | string | No | token field. 10 . |
| `volumeFor24h` | string | No | 24 field. . 10 . |
| `volumeChangeFor24h` | string | No | 24 field. . 10 . |
| `percentChangeFor1h` | string | No | 1 field. . |
| `percentChangeFor24h` | string | No | 24 field. . |
| `percentChangeFor7d` | string | No | 7 field. . |
| `marketCap` | string | No | token field. . 10 . |
| `updatedAt` | string | No | data field. ISO 8601 . |
| `listings` | array | No | token field. |
| `contract` | object | No |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
