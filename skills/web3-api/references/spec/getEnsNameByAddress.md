# getEnsNameByAddress

> Resolves an Ethereum address to its mapped ENS Primary Name.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getEnsNameByAddress

## Supported Chains
- ethereum
- **Networks**: mainnet only

## Endpoint
`POST /{chain}/{network}/ens/getEnsNameByAddress`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (ethereum) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| address | string | Yes | Ethereum address (0x + 40 hex characters) |

## Response

| Field | Type | Description |
|-------|------|-------------|
| name | string | Primary ENS domain name. Returns null if no Primary Name is set. Use getEnsRecordsByAccount for all names. |
| expiryDate | string | ENS domain expiry date |
