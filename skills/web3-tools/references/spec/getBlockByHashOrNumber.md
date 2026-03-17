# getBlockByHashOrNumber

> Get Block by Hash or Number

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/getBlockByHashOrNumber

## Supported Chains

- aptos
- arbitrum
- arc
- base
- bnb
- chiliz
- ethereum
- ethereumclassic
- giwa
- kaia
- luniverse
- optimism
- polygon
- bitcoin
- bitcoincash
- dogecoin

Networks: mainnet, sepolia, testnet, hoodi, kairos, amoy

## Endpoint

`POST /{chain}/{network}/blockchain/getBlockByHashOrNumber`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`, `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`, `bitcoin`, `bitcoincash`, `dogecoin`. Default: `aptos`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `block` | string | Yes | parameter . parameter value latest , block number(10 ), block hash(0x 64 hexadecimal string) (earliest, latest) input . "earliest" , "latest" . Default: `latest`. |

## Response

### Success (200) - Successful Response

**Bitcoin Cash:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `hash` | string | Yes | SHA-256 hash value . creation , chain . |
| `height` | integer | Yes | chain number . 0 , 1 . |
| `version` | integer | Yes | version number , network . version . |
| `timestamp` | integer | Yes | creation , UNIX timestamp . |
| `nonce` | integer | Yes | (Proof-of-Work) value , block hash . |
| `bits` | string | Yes | block hash value , 32 hexadecimal . value network . |
| `difficulty` | string | Yes | , value value . value . |
| `merkleRoot` | string | Yes | transaction hash hash value . data confirmation . |
| `transactionCount` | integer | Yes | transaction . transaction confirmation . |
| `size` | integer | Yes | size , transaction data byte value . value data . |
| `weight` | integer | Yes | SegWit data BIP-141 . |
| `previousBlockHash` | string | Yes | hash value , chain . value null. |
| `nextBlockHash` | string | Yes | hash value , latest block value null . chain . |
| `medianTime` | integer | Yes | 11 timestamp value . . |
| `strippedSize` | integer | Yes | SegWit data size . byte , transaction data size. |
| `transactions` | array | Yes | transaction hash value array . transaction hash value . |
| `ablastate` | object | No | ABLA(Adaptive Block Limit Algorithm) statusvalue . ABLA , . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
