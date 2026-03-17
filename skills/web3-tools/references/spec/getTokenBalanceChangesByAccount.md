# getTokenBalanceChangesByAccount

> Get Token Balance Changes by Account

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getTokenBalanceChangesByAccount

## Supported Chains

- aptos
- xrpl

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/token/getTokenBalanceChangesByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`, `xrpl`. Default: `aptos`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

### Aptos

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `assetTypes` | array | No | parameter . 64 hexadecimal("0x" ) input , : * Coin: "0x1::aptos_coin::AptosCoin" Struct ID * Fungible Asset: Token Metadata Object address ⚠️ assetTypes linkedAssetTypes . |
| `linkedAssetTypes` | array | No | Coin FA(Fungible Asset) . linkedAssetType FA Object address input , 64 hexadecimal("0x" ) input . ⚠️ assetTypes linkedAssetTypes . |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### XRP Ledger

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `currency` | object | No |  |
| `issuer` | object | No |  |
| `fromLedger` | object | No |  |
| `toLedger` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |


## Response

### Success (200) - Successful Response

**Aptos:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**XRP Ledger:**

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
