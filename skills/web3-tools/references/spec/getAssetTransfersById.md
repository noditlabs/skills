# getAssetTransfersById

> Get Asset Transfers By ID

- **Category**: Data API - Asset

## Supported Chains

- tron

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/asset/getAssetTransfersById`

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
| `assetId` | object | Yes |  |
| `fromBlock` | string | No | parameter . block number, block hash block tag input , value 0 . - block number: 10 input . - block hash: 64 hexadecimal string input , 0x . - block tag: fromBlock "earliest" input . : - toBlock fromBlock , fromBlock result . - fromBlock block number toBlock block number . - toBlock fromBlock value input , result . - fromBlock "latest" input . Default: `earliest`. |
| `toBlock` | string | No | parameter . block number, block hash block tag input , value "latest" . - block number: 10 input . - block hash: 64 hexadecimal string input , 0x . - block tag: "latest" input . : - input toBlock blockNumber input fromBlock blockNumber value input . - toBlock fromBlock value input , input result . - fromBlock toBlock , genesis block toBlock input result . - toBlock "earliest" input . Default: `latest`. |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |

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
