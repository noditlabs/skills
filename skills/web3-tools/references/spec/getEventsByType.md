# getEventsByType

> Get Events by Type

- **Category**: Data API - Blockchain

## Supported Chains

- aptos

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/blockchain/getEventsByType`

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
| `eventType` | string | Yes | event parameter . event module event struct . `module_address::module_name::event_name` input . |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . Default: `earliest`. |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |

## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | event transaction hash field. transaction data hashvalue , 0x 64 hexadecimal string . hash event transaction . |
| `transactionVersion` | integer | Yes | transaction version field. chain transaction ID , 0 . transaction execution transaction status . |
| `blockHeight` | integer | Yes | transaction height field. (0) value . value transaction , transaction finalized confirmation . |
| `blockTimestamp` | integer | Yes | creation field. UNIX timestamp , creation . timestamp transaction creation . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
