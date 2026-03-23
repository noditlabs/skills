# getNativeTransfersByAccount

> Get Native Transfers By Account

- **Category**: Data API - Token
- **Official Docs**: https://developer.nodit.io/reference/getNativeTransfersByAccount

## Supported Chains

- arc
- tron

Networks: testnet, mainnet

## Endpoint

`POST /{chain}/{network}/native/getNativeTransfersByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `arc`, `tron`. Default: `arc`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `testnet`, `mainnet`. Default: `testnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | No |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |

### Tron

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | No |  |
| `relation` | object | No |  |
| `fromBlock` | string | No | parameter . block number, block hash block tag input , value 0 . - block number: 10 input . - block hash: 64 hexadecimal string input , 0x . - block tag: fromBlock "earliest" input . : - toBlock fromBlock , fromBlock result . - fromBlock block number toBlock block number . - toBlock fromBlock value input , result . - fromBlock "latest" input . Default: `earliest`. |
| `toBlock` | string | No | parameter . block number, block hash block tag input , value "latest" . - block number: 10 input . - block hash: 64 hexadecimal string input , 0x . - block tag: "latest" input . : - input toBlock blockNumber input fromBlock blockNumber value input . - toBlock fromBlock value input , input result . - fromBlock toBlock , genesis block toBlock input result . - toBlock "earliest" input . Default: `latest`. |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |


## Response

### Success (200) - Successful Response

**Arc:**

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
