# getNextNonceByAccount

> Get Next Nonce by Account

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/getNextNonceByAccount

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

`POST /{chain}/{network}/blockchain/getNextNonceByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`. Default: `arbitrum`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |

## Response

### Success (200) - Successful Response

**Arbitrum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

**Arc:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

**Base:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

**BNB Smart Chain:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

**Chiliz:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

**Ethereum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

**Ethereum Classic:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

**Giwa:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

**Kaia:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

**Luniverse:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

**Optimism:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

**Polygon:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `nonce` | string | Yes | nonce value is returned. value transaction creation 1 , transaction creation value confirmation transaction nonce value . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
