# getNativeTokenBalanceByAccount

> Retrieve the native token balance of a specific account. Supports UTXO-based chains (Bitcoin, Dogecoin, Bitcoincash) and XRPL.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getNativeTokenBalanceByAccount

## Supported Chains
- bitcoin, dogecoin, bitcoincash, xrpl
- Networks: mainnet

## Endpoint
`POST /{chain}/{network}/native/getNativeTokenBalanceByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (bitcoin, dogecoin, bitcoincash, xrpl) |
| network | string | Yes | Target network (mainnet) |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | Yes | Account address. Bitcoin: P2PKH/P2SH/Bech32 format. XRPL: r-prefixed Base58 (25-35 chars). |

## Response

### 200 OK

| Field | Type | Description |
|-------|------|-------------|
| ownerAddress | string | Owner address |
| balance | string | Balance (BTC units for Bitcoin, XRP units for XRPL) |
