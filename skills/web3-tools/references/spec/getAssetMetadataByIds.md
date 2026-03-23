# getAssetMetadataByIds

> Get Asset Metadata By IDs

- **Category**: Data API - Asset
- **Official Docs**: https://developer.nodit.io/reference/getAssetMetadataByIds

## Supported Chains

- tron

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/asset/getAssetMetadataByIds`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `tron`. Default: `tron`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `assetIds` | array | Yes | Asset ID input . Asset ID 0 . |

## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | integer | Yes | TRC10 token ID. ID network TRC10 . |
| `name` | string | Yes | contract . , contract creation ("name") input is returned. |
| `symbol` | string | Yes | contract . , contract creation ("symbol") input is returned. |
| `totalSupply` | string | Yes | contract . value token , 10 . |
| `decimals` | integer | Yes | token . TIP10 "precision" value 0 . |
| `startTime` | integer | Yes | ICO(Initial Coin Offering) . value UNIX timestamp( ) . |
| `endTime` | integer | Yes | ICO . value UNIX timestamp( ) . |
| `description` | string | Yes | TRC10 token . value , data. |
| `url` | string | Yes | TRC10 token URL. value , . |
| `blockNumber` | integer | Yes | TRC10 token creation number. value token creation transaction number , chain transaction . |
| `blockTimestamp` | integer | Yes | TRC10 token creation . UNIX timestamp( ) , value creation confirmation . |
| `transactionHash` | string | Yes | TRC10 token transaction hash value. value TRC10 transaction . |
| `deployer` | string | Yes | TRC10 token address. , . |
| `trxNum` | integer | Yes | TRC10 TRX . value "trx_num/num" , sun. |
| `num` | integer | Yes | TRC10 TRC10 . TRC10 "trx_num/num" . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
