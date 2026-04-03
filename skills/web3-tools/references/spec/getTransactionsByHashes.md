# getTransactionsByHashes

> Get Transactions By Hashes

- **Category**: Data API - Blockchain

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
- tron
- xrpl

Networks: mainnet, sepolia, testnet, hoodi, kairos, amoy

## Endpoint

`POST /{chain}/{network}/blockchain/getTransactionsByHashes`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`, `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`, `tron`, `xrpl`. Default: `aptos`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

### Aptos

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withBalanceChanges` | object | No |  |

### Arbitrum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Base

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### BNB Smart Chain

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Chiliz

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Ethereum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Ethereum Classic

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Giwa

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Kaia

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Luniverse

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Optimism

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Polygon

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Tron

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### XRP Ledger

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHashes` | array | Yes |  |
| `withBalanceChanges` | object | No |  |
| `withTokenTransfers` | object | No |  |


## Response

### Success (200) - Successful Response

**Arbitrum (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash field. 0x 64 hexadecimal string . |
| `transactionIndex` | integer | Yes | transaction index field. . |
| `blockHash` | string | Yes | hash field. 0x 64 hexadecimal string . |
| `blockNumber` | integer | Yes | block number field. |
| `from` | string | Yes | transaction address field. 0x 40 hexadecimal string . |
| `to` | string | Yes | transaction address field. contract creation transaction null is returned.0x 40 hexadecimal string . |
| `value` | string | Yes | transaction token field. 10 . |
| `input` | string | Yes | transaction data field. Native Token(ETH, MATIC ) . 0x hexadecimal string . |
| `decodedInput` | object | No | transaction input result field. withDecode parameter true input , input execution function data . function withDecode true . |
| `functionSelector` | string | Yes | function 4byte function value . function function Keccak-256 result 4byte . 0x 8 hexadecimal string . |
| `nonce` | string | Yes | transaction nonce value field. transaction . 10 . |
| `gas` | string | Yes | transaction execution field. 10 . |
| `gasPrice` | string | Yes | field. EIP-1559(London Hard fork) transaction ( fee) , network . 10 . |
| `maxFeePerGas` | string | No | fee field. baseFeePerGas MaxPriorityFeePerGas . EIP-1559(London Hard fork) fee . transaction . 10 . |
| `maxPriorityFeePerGas` | string | No | creation fee . value creation transaction . EIP-1559(London Hard fork) fee . transaction . 10 . |
| `gasUsed` | string | Yes | transaction execution field. 10 . |
| `cumulativeGasUsed` | string | Yes | transaction , transaction field. 10 . |
| `effectGasPrice` | string | No | transaction field. EIP-1559(London Hard fork) fee . transaction . 10 . |
| `contractAddress` | string | Yes | transaction contract creation transaction , creation contract address field. 0x 40 hexadecimal string . |
| `type` | string | No | transaction , . 10 . 0: value transaction. EIP-2718 transaction . 1: EIP-2930 'Access List' transaction. transaction address slot . 2: EIP-1559 'Fee Market' transaction. transaction , maxFeePerGas maxPriorityFeePerGas . 3: EIP-4844 'Blob Transaction'. transaction blob data , (Rollup) Layer2 data . 4: EIP-7702 transaction , signature/ authorizationList . signature authentication . |
| `status` | string | No | transaction status field. 1 , 0 . Byzantium Hard Fork transaction . 10 . |
| `logsBloom` | string | Yes | transaction field. 0x 512 hexadecimal string . |
| `accessList` | array | No | transaction field. |
| `timeStamp` | integer | No | transaction creation field. UNIX timestamp . |
| `authorizationList` | array | No | transaction signature . signature chain ID, nonce, signaturevalue , EIP-7702 . network , transaction ( : type 4 ) transaction . |
| `logs` | array | No | transaction field. withLogs parameter true . |

**Tron (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `transactionHash` | string | Yes | transaction hash value . prefix(0x) 64 hexadecimal string . |
| `transactionIndex` | integer | Yes | transaction , transaction execution . |
| `transactionTimestamp` | integer | Yes | transaction creation . transaction creation transaction , status transaction block timestamp . |
| `blockNumber` | integer | Yes | . chain creation . |
| `blockTimestamp` | integer | Yes | creation timestamp . Unix timestamp . |
| `refBlockBytes` | string | Yes | transaction . 6 7 byte 2 byte size . finalized , value transaction transaction . |
| `refBlockHash` | string | Yes | transaction . block hash 8 15 byte 8 byte size . finalized , value transaction transaction . |
| `type` | string | Yes | transaction . transaction , network transaction . TransferContract, TriggerSmartContract , TRX , contract execution . |
| `typeUrl` | string | Yes | transaction . chain (chain Buffers) transaction . |
| `isMultiSig` | boolean | Yes | transaction (Multi-Signature) transaction field. signature transaction , height . |
| `from` | string | Yes | transaction creation sender address. , transaction address . "T" 34 base58 . |
| `to` | string | Yes | transaction recipient address. transaction TRX address contract . "T" 34 base58 . |
| `value` | string | Yes | transaction . TRX TRC10 token . <strong style='color: red;'>*</strong> "assetId" value . "assetId" 0 TRX , value 0 TRC10 token . (e.g., TRX sun) , 10 . |
| `assetId` | integer | Yes | token(TRX, TRC10) value . <strong style='color: red;'>*</strong> "assetId" 0 TRX , value 0 TRC10 token . |
| `input` | string | Yes | contract data input value value . contract function parameter value , contract . |
| `functionSelector` | string | Yes | execution function . , transfer(address,uint256) function keccak-256 hashvalue creation , hashvalue 4byte function selector . |
| `result` | string | Yes | transaction count result status. transaction result , transaction confirmation . status SUCCESS, FAILED value . <strong style='color: red;'>*</strong> contract execution transaction chain transaction . |
| `contractRet` | string | Yes | contract execution result , transaction . - : SUCCESS, REVERT, BAD_JUMP_DESTINATION, OUT_OF_MEMORY, PRECOMPILED_CONTRACT, ... |
| `resMessage` | string | Yes | transaction execution , . transaction is returned. |
| `fee` | string | Yes | transaction execution TRX . transaction creation (Bandwidth) (Energy) , TRX . , netFee energyFee value . , fee 0 . TRX . "sun" , 1 TRX = 1,000,000 sun. |
| `feeLimit` | string | Yes | transaction creation fee , transaction execution fee is specified. fee feeLimit transaction . fee . "sun" , 1 TRX = 1,000,000 sun. |
| `netFee` | string | Yes | transaction creation (Bandwidth) TRX . netFee . "sun" , 1 TRX = 1,000,000 sun. |
| `netUsage` | string | Yes | transaction (Bandwidth) . transaction creation , TRX , TRX netFee . |
| `energyFee` | string | Yes | transaction creation (Energy) , TRX . contract execution creation . "sun" , 1 TRX = 1,000,000 sun. |
| `energyUsage` | string | Yes | transaction creation (Energy) . |
| `originEnergyUsage` | string | Yes | contract deployment (Energy) . contract deployment . |
| `energyUsageTotal` | string | Yes | transaction (Energy) . transaction creation (energyUsage) contract deployment (originEnergyUsage) , transaction execution . |
| `energyPenaltyTotal` | string | Yes | contract (Energy) . network ( ) , contract . |
| `permissionId` | integer | No | transaction . - 0: Owner . - 1: Witness . creation , transaction signature . - 2 : Active . transaction execution . |
| `assetIssueId` | integer | No | transaction TRC10 value . transaction AssetIssueContract TRC10 asset ID , transaction null is returned. |
| `withdrawAmount` | string | No | reward sun . reward (withdrawal reward) transaction (unfreeze) transaction , vote reward . "sun" , 1 TRX = 1,000,000 sun. |
| `withdrawExpireAmount` | string | No | Stake2.0 transaction , TRX . "sun" , 1 TRX = 1,000,000 sun . 1. (unstaking) transaction 2. (unfrozen) balance transaction 3. transaction |
| `unfreezeAmount` | string | No | Stake1.0 (unstaking) transaction , TRX , "sun" , 1 TRX = 1,000,000 sun. |
| `cancelUnfreezeV2Amount` | object | No | (BANDWIDTH), (ENERGY), (TRON POWER) TRX . |
| `exchangeId` | integer | No | network (DEX) (Swap) ID . ID transaction , . |
| `exchangeReceivedAmount` | string | No | network (DEX) (Swap) . |
| `exchangeInjectAnotherAmount` | string | No | network (DEX) (Swap) . |
| `exchangeWithdrawAnotherAmount` | string | No | network (DEX) (Swap) . |
| `decodedInput` | object | No | contract input data(input) ABI value . Native Token(TRX) contract input data . <strong style='color: red;'>*</strong> withDecode true . |

**XRP Ledger (array of objects):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ledgerIndex` | integer | Yes | transaction Ledger . transaction Ledger confirmation . |
| `ledgerTimestamp` | integer | Yes | value transaction Ledger close time Unix timestamp result is returned. XRP Ledger close time Ripple Epoch(2000 1 1 00:00 UTC) . , Unix timestamp Unix Epoch(1970 1 1 00:00 UTC) , 946,684,800 . ledgerTimestamp Ledger close time 946,684,800 . |
| `transactionIndex` | integer | Yes | Ledger transaction index . value Ledger transaction . |
| `transactionHash` | string | Yes | transaction 256 (64 hexadecimal) hashvalue . transaction data . |
| `transactionType` | string | Yes | transaction . Payment, OfferCreate, EscrowCreate transaction , . |
| `transactionResult` | string | Yes | transaction result , 'tesSUCCESS' result code . transaction confirmation . |
| `account` | string | Yes | transaction account address . account address 25~35 Base58 encoding , 'r' . |
| `sequence` | integer | Yes | transaction number , . |
| `lastLedgerSequence` | integer | No | transaction Ledger . value Ledger transaction . |
| `ticketSequence` | integer | No | transaction , number value . transaction . |
| `signingPubKey` | string | Yes | transaction signature key , 33byte(66 hexadecimal) key . |
| `txnSignature` | string | No | signingPubKey creation transaction signature value . signature transaction authentication . |
| `fee` | string | Yes | transaction fee , XRP (XRP ) . value XRP , 1 XRP 1,000,000 drop . |
| `flags` | string | No | transaction value. , value 0 . |
| `accountTxnId` | string | No | transaction 256 hashvalue . value , transaction transaction ID . transaction , transaction status confirmation . |
| `sourceTag` | integer | No | transaction 32 value . address( : ) . , recipient " " . |
| `signers` | array | No | signature transaction , signature object array . object signature , signature key, signature value . |
| `memos` | array | No | transaction data object array . object , . |
| `transactionCategory` | string | Yes | transaction . value AMM, Check, Escrow, Offer, Payment, Payment Channel , transaction ( : Payment, OfferCreate ) . |
| `transactionDetails` | object | No | transaction object . object transaction data . |
| `balanceChanges` | object | No |  |
| `tokenTransfers` | object | No |  |
| `balanceOutAccounts` | array | No | transaction · result, 0 ( ) account address . XRP IOU token . |
| `balanceInAccounts` | array | No | transaction · result, 0 ( ) account address . XRP IOU token . |
| `balanceChangedTokens` | array | No | transaction 0 token . 'currency-issuer' . |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
