# getEnsRecordsByAccount

> Get ENS Records By Account

- **Category**: Data API - ENS
- **Official Docs**: https://developer.nodit.io/reference/getEnsRecordsByAccount

## Supported Chains

- ethereum

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/ens/getEnsRecordsByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `ethereum`. Default: `ethereum`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
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
| `name` | string | Yes | ENS field. |
| `isMigrated` | boolean | Yes | ENS latest version field. true latest version , false . . |
| `isPrimaryName` | boolean | Yes | ENS Primary Name field. ENS address , Primary Name . true Primary Name , false Primary Name . |
| `node` | string | Yes | ENS , namehash creation hashvalue field. , example.nodit.eth , node value namehash('example.nodit.eth') creation . 0x 64 hexadecimal string . |
| `labelName` | string | Yes | field. , example.nodit.eth , labelName 'example'. |
| `labelHash` | string | Yes | hashvalue field. , example.nodit.eth , labelHash keccak256('example') creation . 0x 64 hexadecimal string . <br/> <strong style='color: red;'>*</strong> ownerAddress address contract address . address confirmation wrappedOwnerAddress . |
| `ownerAddress` | string | Yes | ENS address field. 0x 40 hexadecimal string . <br/> <strong style='color: red;'>*</strong> address , address . resolver resolvedAddress . |
| `resolver` | object | Yes | Resolver field. |
| `registration` | object | Yes | field. |
| `nameWrapper` | object | Yes | field. ownerAddress contract address . address confirmation wrappedOwnerAddress . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
