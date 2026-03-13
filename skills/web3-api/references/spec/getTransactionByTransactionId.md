# getTransactionByTransactionId

> Retrieves detailed information about a specific transaction using its transaction ID (UTXO chains).

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getTransactionByTransactionId

## Supported Chains
- bitcoin, dogecoin, bitcoincash
- **Networks**: mainnet, testnet

## Endpoint
`POST /{chain}/{network}/blockchain/getTransactionByTransactionId`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain (bitcoin, dogecoin, bitcoincash) |
| network | string | Yes | Target network (mainnet, testnet) |

## Request Body

| Name | Type | Required | Description |
|------|------|----------|-------------|
| transactionId | string | Yes | Transaction ID to query (64-character hex string without 0x prefix) |

## Response

| Field | Type | Description |
|-------|------|-------------|
| id | string | Unique transaction identifier |
| index | integer | Transaction index within the block |
| hash | string | Transaction hash (includes SegWit data) |
| version | integer | Transaction version |
| lockTime | integer | Lock time (block height or UNIX timestamp) |
| size | integer | Transaction size in bytes |
| vsize | integer | Virtual size in bytes (SegWit-adjusted) |
| weight | integer | Transaction weight per BIP-141 |
| fee | integer | Transaction fee |
| vinCount | integer | Number of inputs (Vin) |
| voutCount | integer | Number of outputs (Vout) |
| blockHeight | integer | Block height containing the transaction |
| blockHash | string | Block hash |
| blockTimestamp | integer | Block creation UNIX timestamp |
| vin | object | Input transaction details (address, value, scriptSig, witness, etc.) |
| vout | object | Output transaction details (address, value, scriptPubKey, etc.) |
