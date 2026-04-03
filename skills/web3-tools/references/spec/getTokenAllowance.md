# getTokenAllowance

> Get Token Allowance

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

`POST /{chain}/{network}/token/getTokenAllowance`

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
| `contractAddress` | string | Yes | contract address parameter . 0x 40 hexadecimal string input . |
| `ownerAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `spenderAddress` | object | Yes |  |

## Response

### Success (200) - Successful Response

**Arbitrum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**Arc:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**Base:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**BNB Smart Chain:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**Chiliz:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**Ethereum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**Ethereum Classic:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**Giwa:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**Kaia:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**Luniverse:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**Optimism:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**Polygon:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

**Tron:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `allowance` | string | No | spender owner transferFrom token is returned. value approve transferFrom . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
