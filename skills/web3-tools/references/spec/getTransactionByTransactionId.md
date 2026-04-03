# getTransactionByTransactionId

> Get Transaction By Transaction ID

- **Category**: Data API - Blockchain

## Supported Chains

- bitcoin
- bitcoincash
- dogecoin

Networks: mainnet

## Endpoint

`POST /{chain}/{network}/blockchain/getTransactionByTransactionId`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `bitcoin`, `bitcoincash`, `dogecoin`. Default: `bitcoin`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionId` | string | Yes | transaction ID parameter . 0x 64 hexadecimal string input . |

## Response

### Success (200) - Successful Response

**Bitcoin:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | transaction , transaction value. |
| `index` | integer | Yes | transaction index. 0 , transaction . |
| `hash` | string | Yes | transaction hash value , transaction data . SegWit data . |
| `version` | integer | Yes | transaction version value , transaction . |
| `lockTime` | integer | Yes | transaction , transaction (block height UNIX timestamp). value `0` transaction . |
| `size` | integer | Yes | transaction size(byte) , transaction data . |
| `vsize` | integer | Yes | transaction size(byte) , SegWit data transaction size. BIP-141 (weight) 4 value. |
| `weight` | integer | Yes | transaction , BIP-141 transaction network . `(non-witness size * 3) + total size` . |
| `fee` | integer | Yes | transaction fee(BTC ) , input value output value value. |
| `vinCount` | integer | Yes | input(Vin) transaction . |
| `voutCount` | integer | Yes | output(Vout) transaction . |
| `blockHeight` | integer | Yes | transaction height. |
| `blockHash` | string | Yes | transaction hash value. |
| `blockTimestamp` | integer | Yes | transaction creation , UNIX timestamp . |
| `vin` | object | No |  |
| `vout` | object | No |  |

**Bitcoin Cash:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | transaction , transaction value. |
| `index` | integer | Yes | transaction index. 0 , transaction . |
| `hash` | string | Yes | transaction hash value , transaction data . SegWit data . |
| `version` | integer | Yes | transaction version value , transaction . |
| `lockTime` | integer | Yes | transaction , transaction (block height UNIX timestamp). value `0` transaction . |
| `size` | integer | Yes | transaction size(byte) , transaction data . |
| `vsize` | integer | Yes | transaction size(byte) , SegWit data transaction size. BIP-141 (weight) 4 value. |
| `weight` | integer | Yes | transaction , BIP-141 transaction network . `(non-witness size * 3) + total size` . |
| `fee` | integer | Yes | transaction fee(BTC ) , input value output value value. |
| `vinCount` | integer | Yes | input(Vin) transaction . |
| `voutCount` | integer | Yes | output(Vout) transaction . |
| `blockHeight` | integer | Yes | transaction height. |
| `blockHash` | string | Yes | transaction hash value. |
| `blockTimestamp` | integer | Yes | transaction creation , UNIX timestamp . |
| `vin` | object | No |  |
| `vout` | object | No |  |

**Dogecoin:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | transaction , transaction value. |
| `index` | integer | Yes | transaction index. 0 , transaction . |
| `hash` | string | Yes | transaction hash value , transaction data . SegWit data . |
| `version` | integer | Yes | transaction version value , transaction . |
| `lockTime` | integer | Yes | transaction , transaction (block height UNIX timestamp). value `0` transaction . |
| `size` | integer | Yes | transaction size(byte) , transaction data . |
| `vsize` | integer | Yes | transaction size(byte) , SegWit data transaction size. BIP-141 (weight) 4 value. |
| `weight` | integer | Yes | transaction , BIP-141 transaction network . `(non-witness size * 3) + total size` . |
| `fee` | integer | Yes | transaction fee(BTC ) , input value output value value. |
| `vinCount` | integer | Yes | input(Vin) transaction . |
| `voutCount` | integer | Yes | output(Vout) transaction . |
| `blockHeight` | integer | Yes | transaction height. |
| `blockHash` | string | Yes | transaction hash value. |
| `blockTimestamp` | integer | Yes | transaction creation , UNIX timestamp . |
| `vin` | object | No |  |
| `vout` | object | No |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
