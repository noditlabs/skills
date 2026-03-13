# getAssetMetadataByIds

> Retrieves TRC10 token metadata by Asset IDs. Returns up to 100 results per call.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getAssetMetadataByIds

## Supported Chains
- tron
- **Networks**: mainnet

## Endpoint
`POST /{chain}/{network}/asset/getAssetMetadataByIds`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (tron) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| assetIds | array | Yes | Array of Asset IDs (positive integers) |

## Response

Returns an array of TRC10 metadata objects:

| Field | Type | Description |
|-------|------|-------------|
| id | integer | TRC10 token unique ID |
| name | string | Token name |
| symbol | string | Token symbol |
| totalSupply | string | Total supply (decimal string) |
| decimals | integer | Decimal places |
| startTime | integer | ICO start time (UNIX ms) |
| endTime | integer | ICO end time (UNIX ms) |
| description | string | Token description |
| url | string | Token URL |
| blockNumber | integer | Creation block number |
| blockTimestamp | integer | Creation timestamp (UNIX ms) |
| transactionHash | string | Creation transaction hash |
| deployer | string | Issuer address |
| trxNum | integer | TRX quantity for value ratio (SUN) |
| num | integer | TRC10 quantity for value ratio |
