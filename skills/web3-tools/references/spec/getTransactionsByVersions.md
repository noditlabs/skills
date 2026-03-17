# getTransactionsByVersions

> Get Transactions By Versions

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/getTransactionsByVersions

## Supported Chains

- aptos

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/blockchain/getTransactionsByVersions`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`. Default: `aptos`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionVersions` | array | Yes | transaction version array input. |
| `withBalanceChanges` | object | No |  |

## Response

### Success (200) - Successful Response

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction field. transaction data(signature payload) hashvalue , 0x 64 hexadecimal string . transaction transaction . |
| `transactionVersion` | integer | Yes | transaction version field. chain transaction ID , 0 . transaction execution transaction status . |
| `blockHeight` | integer | Yes | transaction height field. (0) value . value transaction , transaction finalized confirmation . |
| `blockTimestamp` | integer | Yes | transaction creation field. UNIX timestamp , value creation transaction . |
| `expirationTimestampSecs` | integer | Yes | transaction field. UNIX timestamp , transaction chain . transaction transaction . |
| `gasUnitPrice` | string | Yes | transaction field. Octas(1 APT = 10^8 Octas) , . transaction transaction count . |
| `gasUsed` | string | Yes | transaction execution field. transaction . transaction count gasUsed * gasUnitPrice . |
| `maxGasAmount` | string | Yes | transaction field. transaction execution value transaction , . fee . |
| `secondarySigners` | array | Yes | signature transaction signature address field. signature (sender) transaction signature address . transaction . |
| `sender` | string | Yes | transaction address field. 0x 64 hexadecimal string , transaction . transaction count number . |
| `sequenceNumber` | integer | Yes | sender number field. 0 transaction 1 , transaction . number transaction execution . |
| `success` | boolean | Yes | transaction execution field. true transaction execution , false execution . |
| `vmStatus` | string | Yes | transaction execution result status field. 'Executed successfully' , . transaction . |
| `events` | array | Yes | transaction execution event field. event transaction status execution . transaction . |
| `balanceInAccounts` | array | Yes | transaction address field. balanceChanges value( ) address . recipient . |
| `balanceOutAccounts` | array | Yes | transaction address field. balanceChanges value( ) address . . |
| `balanceChangedTokens` | array | Yes | transaction balance token field. token 'moduleaddress::module :: ' . transaction . |
| `balanceChanges` | object | No |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
