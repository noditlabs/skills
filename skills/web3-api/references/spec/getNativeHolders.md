# getNativeHolders

> Retrieve the list of native token holders including their addresses and balances.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getNativeHolders

## Supported Chains
- tron
- Networks: mainnet

## Endpoint
`POST /{chain}/{network}/native/getNativeHolders`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (tron) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| page | integer | No | Page number (max 100). Cannot be used with cursor. |
| rpp | integer | No | Results per page (1-1000) |
| cursor | string | No | Cursor for pagination. Cannot be used with page. |
| withCount | boolean | No | Include total count in response (default: false, may slow response) |

## Response

### 200 OK

| Field | Type | Description |
|-------|------|-------------|
| page | integer | Current page number |
| rpp | integer | Results per page |
| cursor | string | Cursor for next page |
| count | integer | Total count (only if withCount=true) |
| items | array | List of holders |

### Items

| Field | Type | Description |
|-------|------|-------------|
| ownerAddress | string | Holder's address |
| balance | string | Balance in smallest unit (SUN for TRX) |
