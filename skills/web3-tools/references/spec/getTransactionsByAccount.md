# getTransactionsByAccount

> Get Transactions By Account

- **Category**: Data API - Blockchain
- **Official Docs**: https://developer.nodit.io/reference/getTransactionsByAccount

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
- tron
- xrpl

Networks: mainnet, sepolia, testnet, hoodi, kairos, amoy

## Endpoint

`POST /{chain}/{network}/blockchain/getTransactionsByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `aptos`, `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`, `bitcoin`, `bitcoincash`, `dogecoin`, `tron`, `xrpl`. Default: `aptos`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

### Aptos

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address from to transaction filter parameter . from to, both , parameter value both . - from: address balanceOutAccounts result is returned. - to: address balanceInAccounts result is returned. - both: address result is returned. Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withBalanceChanges` | object | No |  |

### Arbitrum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Base

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### BNB Smart Chain

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Chiliz

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Ethereum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Ethereum Classic

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Giwa

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Kaia

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Luniverse

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Optimism

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Polygon

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `fromBlock` | object | No |  |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### Bitcoin

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Bitcoin Cash

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Dogecoin

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |

### Tron

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromBlock` | string | No | parameter . block number, block hash block tag input , value 0 . - block number: 10 input . - block hash: 64 hexadecimal string input , 0x . - block tag: fromBlock "earliest" input . : - toBlock fromBlock , fromBlock result . - fromBlock block number toBlock block number . - toBlock fromBlock value input , result . - fromBlock "latest" input . Default: `earliest`. |
| `toBlock` | string | No | parameter . block number, block hash block tag input , value "latest" . - block number: 10 input . - block hash: 64 hexadecimal string input , 0x . - block tag: "latest" input . : - input toBlock blockNumber input fromBlock blockNumber value input . - toBlock fromBlock value input , input result . - fromBlock toBlock , genesis block toBlock input result . - toBlock "earliest" input . Default: `latest`. |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withLogs` | object | No |  |
| `withDecode` | object | No |  |

### XRP Ledger

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `fromLedger` | object | No |  |
| `toLedger` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withBalanceChanges` | object | No |  |
| `withTokenTransfers` | object | No |  |


## Response

### Success (200) - Successful Response

**Aptos:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Arbitrum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Arc:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Base:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**BNB Smart Chain:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Chiliz:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Ethereum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Ethereum Classic:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Giwa:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Kaia:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Luniverse:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Optimism:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Polygon:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Bitcoin:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Bitcoin Cash:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Dogecoin:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**Tron:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

**XRP Ledger:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `items` | array | No |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
