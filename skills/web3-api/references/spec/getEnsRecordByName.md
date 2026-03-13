# getEnsRecordByName

> Retrieves detailed ENS domain record information by domain name.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getEnsRecordByName

## Supported Chains
- ethereum
- **Networks**: mainnet only

## Endpoint
`POST /{chain}/{network}/ens/getEnsRecordByName`

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
| name | string | ENS domain name |
| isMigrated | boolean | Whether migrated to latest ENS version |
| isPrimaryName | boolean | Whether this is the Primary Name |
| node | string | Namehash identifier (0x + 64 hex) |
| labelName | string | Lowest-level label (e.g., "example" for example.eth) |
| labelHash | string | Keccak256 hash of the label |
| ownerAddress | string | Domain owner address |
| resolver | object | Resolver info: contractAddress, resolvedAddress, contentHash, text records |
| registration | object | Registration info: registrantAddress, registrationDate, expiryDate, cost (Wei) |
| nameWrapper | object | Wrapper info: contractAddress, wrappedOwnerAddress (null if unwrapped) |
