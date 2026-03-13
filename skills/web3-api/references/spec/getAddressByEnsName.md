# getAddressByEnsName

> Resolves an ENS domain name to its mapped Ethereum address.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getAddressByEnsName

## Supported Chains
- ethereum
- **Networks**: mainnet only

## Endpoint
`POST /{chain}/{network}/ens/getAddressByEnsName`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (ethereum) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| name | string | No | ENS domain name (e.g., "vitalik.eth") |

## Response

| Field | Type | Description |
|-------|------|-------------|
| address | string | Ethereum address the ENS domain points to. Returns null if domain does not exist. Expired domains may still return the previous address. |
| expiryDate | string | ENS domain expiry date |
