# getAssetMetadataByIssuer

> Retrieves TRC10 token metadata issued by a specific address.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getAssetMetadataByIssuer

## Supported Chains
- tron
- **Networks**: mainnet

## Endpoint
`POST /{chain}/{network}/asset/getAssetMetadataByIssuer`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (tron) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| issuer | string | Yes | Issuer address (T + 33 Base58 string) |

## Response

Returns a TRC10 metadata object with: id, name, symbol, totalSupply, decimals, startTime, endTime, description, url, blockNumber, blockTimestamp, transactionHash, deployer, trxNum, num.
