# getUnspentTransactionOutputsByAccount

> Retrieve the UTXO (Unspent Transaction Output) list for a specific account on Bitcoin-based chains.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getUnspentTransactionOutputsByAccount

## Supported Chains
- bitcoin, dogecoin, bitcoincash
- Networks: mainnet, testnet

## Endpoint
`POST /{chain}/{network}/blockchain/getUnspentTransactionOutputsByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (bitcoin, dogecoin, bitcoincash) |
| network | string | Yes | Target network (mainnet, testnet) |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| accountAddress | string | Yes | Account address (P2PKH, P2SH, Bech32, or Bech32m format) |
| page | integer | No | Page number (max 100) |
| rpp | integer | No | Results per page (1-1000) |
| cursor | string | No | Cursor for pagination |
| withCount | boolean | No | Include total count (default: false) |

## Response

### 200 OK (Paginated)

Items contain:

| Field | Type | Description |
|-------|------|-------------|
| transactionId | string | Transaction ID that created this UTXO |
| voutIndex | integer | Output index in the transaction (0-based) |
| address | string | Receiving address |
| value | string | UTXO value in BTC (1 BTC = 100,000,000 satoshi) |
| blockHeight | integer | Block height |
| blockHash | string | Block hash (64-char hex) |
| blockTimestamp | integer | Block creation time (Unix timestamp) |
