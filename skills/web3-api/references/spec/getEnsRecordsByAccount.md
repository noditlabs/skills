# getEnsRecordsByAccount

> Retrieves ENS domain records associated with an account (by owner or resolved address).

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getEnsRecordsByAccount

## Supported Chains
- ethereum
- **Networks**: mainnet only

## Endpoint
`POST /{chain}/{network}/ens/getEnsRecordsByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (ethereum) |
| network | string | Yes | Target network (mainnet) |

## Request Body

One of the following is required (oneOf):

| Name | Type | Required | Description |
|------|------|----------|-------------|
| ownerAddress | string | Yes* | ENS domain owner address (0x + 40 hex) |
| resolvedAddress | string | Yes* | Address the ENS domain points to (0x + 40 hex) |

Pagination parameters:

| Name | Type | Required | Description |
|------|------|----------|-------------|
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (max 1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count. Default: false |

## Response

| Field | Type | Description |
|-------|------|-------------|
| page | integer | Current page number |
| rpp | integer | Results per page |
| cursor | string | Next page cursor |
| count | integer | Total count (if withCount=true) |
| items | array | List of ENS record objects (name, node, ownerAddress, resolver, registration, nameWrapper, etc.) |
