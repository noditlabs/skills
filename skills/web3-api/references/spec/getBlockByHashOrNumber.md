# getBlockByHashOrNumber

> Retrieve block information by block hash or block number. Supports EVM chains, Bitcoin-based chains, and Aptos.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getBlockByHashOrNumber

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, bitcoin, dogecoin, bitcoincash, aptos
- Networks: mainnet, testnet, sepolia, hoodi, amoy

## Endpoint
`POST /{chain}/{network}/blockchain/getBlockByHashOrNumber`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network |

## Request Body

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| block | string | Yes | Block identifier: block number (decimal), block hash (0x-prefixed 64-char hex for EVM, plain 64-char hex for Bitcoin), or tag (`earliest`, `latest`) |

## Response

### 200 OK - EVM

| Field | Type | Description |
|-------|------|-------------|
| hash | string | Block hash (0x-prefixed 64-char hex) |
| number | integer | Block number |
| timestamp | integer | Unix timestamp |
| parentHash | string | Parent block hash |
| nonce | string | PoW nonce (0x0000000000000000 after PoS) |
| stateRoot | string | State root hash |
| receiptsRoot | string | Receipts root hash |
| transactionsRoot | string | Transactions root hash |
| miner | string | Miner/validator address |
| difficulty | string | Block difficulty (0 after PoS) |
| totalDifficulty | string | Cumulative difficulty |
| gasLimit | string | Max gas allowed (hex) |
| gasUsed | string | Gas used (hex) |
| baseFeePerGas | string | Base fee (hex, post-EIP-1559) |
| size | string | Block size in bytes (hex) |
| transactionCount | integer | Number of transactions |
| transactions | array | Transaction hashes |
| withdrawals | array | Validator withdrawal list |

### 200 OK - Bitcoin/Dogecoin/Bitcoincash

| Field | Type | Description |
|-------|------|-------------|
| hash | string | Block hash (SHA-256) |
| height | integer | Block height |
| version | integer | Block version |
| timestamp | integer | Unix timestamp |
| nonce | integer | PoW nonce |
| bits | string | Difficulty target |
| difficulty | string | Block difficulty |
| merkleRoot | string | Merkle root hash |
| transactionCount | integer | Transaction count |
| size | integer | Block size (bytes) |
| weight | integer | Block weight (BIP-141) |
| previousBlockHash | string | Previous block hash |
| nextBlockHash | string | Next block hash |
| transactions | array | Transaction hashes |

### 200 OK - Aptos

| Field | Type | Description |
|-------|------|-------------|
| hash | string | Block hash (0x-prefixed) |
| height | integer | Block height |
| timestamp | integer | Microsecond Unix timestamp |
| firstVersion | integer | First transaction version |
| lastVersion | integer | Last transaction version |
| transactionsCount | integer | Transaction count |
| transactions | array | Transaction version numbers |
