# getLedgerByHashOrIndex

> Retrieve detailed information about an XRP Ledger by its hash or index.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getLedgerByHashOrIndex

## Supported Chains
- xrpl
- Networks: mainnet, testnet

## Endpoint
`POST /{chain}/{network}/blockchain/getLedgerByHashOrIndex`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (xrpl) |
| network | string | Yes | Target network (mainnet, testnet) |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| ledger | string | Yes | Ledger identifier: ledger index (decimal), ledger hash (64-char hex, no 0x prefix), or tag (`earliest`, `latest`) |

## Response

### 200 OK

| Field | Type | Description |
|-------|------|-------------|
| ledgerHash | string | Ledger hash (64-char hex) |
| ledgerIndex | integer | Ledger sequence number |
| ledgerTimestamp | integer | Unix timestamp (converted from Ripple Epoch) |
| parentLedgerHash | string | Previous ledger hash |
| accountHash | string | Hash of all account states |
| totalCoins | string | Total XRP in the ledger (XRP units) |
| transactionHash | string | Merkle root hash of all transactions |
| transactionCount | integer | Number of transactions |
| transactions | array | Array of transaction hashes (64-char hex strings) |
