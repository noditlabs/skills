# getTokenBalanceChangesByAssetType

> Get Token Balance Changes by Asset Type

- **Category**: Data API - Token

## Supported Chains

- aptos

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/token/getTokenBalanceChangesByAssetType`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`. Default: `aptos`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `assetType` | object | No | parameter . 64 hexadecimal("0x" ) input , : * Coin: "0x1::aptos_coin::AptosCoin" Struct ID * Fungible Asset: Token Metadata Object address ⚠️ assetType linkedAssetType input , parameter . |
| `linkedAssetType` | object | No | Coin FA(Fungible Asset) . linkedAssetType FA Object address input , 64 hexadecimal("0x" ) input . ⚠️ assetType linkedAssetType input , parameter . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . Default: `earliest`. |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |

## Response

### Success (200) - Successful Response

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
