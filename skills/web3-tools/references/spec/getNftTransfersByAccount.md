# getNftTransfersByAccount

> Get NFT Transfers By Account

- **Category**: Data API - NFT
- **Official Docs**: https://developer.nodit.io/reference/getNftTransfersByAccount

## Supported Chains

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

Networks: mainnet, sepolia, testnet, hoodi, kairos, amoy

## Endpoint

`POST /{chain}/{network}/nft/getNftTransfersByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`. Default: `arbitrum`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Demo key: `nodit-demo` |

## Request Body

`Content-Type: application/json`

### Arbitrum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withMetadata` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withFunction` | boolean | No | function parameter . parameter true input , . Default: `False`. |

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withMetadata` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withFunction` | boolean | No | function parameter . parameter true input , . Default: `False`. |

### Base

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withMetadata` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withFunction` | boolean | No | function parameter . parameter true input , . Default: `False`. |

### BNB Smart Chain

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withMetadata` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withFunction` | boolean | No | function parameter . parameter true input , . Default: `False`. |

### Chiliz

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withMetadata` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withFunction` | boolean | No | function parameter . parameter true input , . Default: `False`. |

### Ethereum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withMetadata` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withFunction` | boolean | No | function parameter . parameter true input , . Default: `False`. |

### Ethereum Classic

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withMetadata` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withFunction` | boolean | No | function parameter . parameter true input , . Default: `False`. |

### Giwa

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withMetadata` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withFunction` | boolean | No | function parameter . parameter true input , . Default: `False`. |

### Kaia

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | object | No |  |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . Kaia , "earliest" input Kaia . - Mainnet: 162,900,480 (Aug 29, 2024 11:08:01 UTC+9) - Kairos(Testnet): 156,660,000 (June 13, 2024 10:15:19 UTC+9) |
| `toBlock` | object | No |  |
| `fromDate` | object | No |  |
| `toDate` | object | No |  |
| `withMetadata` | object | No |  |
| `withZeroValue` | object | No |  |
| `withFunction` | object | No |  |

### Luniverse

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withMetadata` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withFunction` | boolean | No | function parameter . parameter true input , . Default: `False`. |

### Optimism

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withMetadata` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withFunction` | boolean | No | function parameter . parameter true input , . Default: `False`. |

### Polygon

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | object | Yes |  |
| `relation` | string | No | account address recipient transaction filter parameter . - from: filter . - to: recipient filter . - both( value): from to transaction . Enum: `from`, `to`, `both`. Default: `both`. |
| `contractAddresses` | object | No |  |
| `fromBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - toBlock , latest block result . - fromBlock value toBlock value . - fromBlock toBlock value input , . - fromBlock "latest" toBlock "latest" . |
| `toBlock` | string | No | parameter . input : - block number: 10 block number input. - block hash: 64 hexadecimal("0x" ). - block tag: "earliest" "latest" latest block . : - fromBlock , genesis block result . - toBlock value fromBlock value . - fromBlock toBlock value input , . - toBlock "earliest" fromBlock "earliest" . |
| `fromDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - toDate , latest block result . - fromDate value toDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `toDate` | string | No | parameter . ISO 8601 (YYYY-MM-DDThh:mm:ss{time zone}) , input . : - fromDate , genesis block result . - toDate value fromDate value value . - fromDate toDate value input , . - fromBlock, toBlock . |
| `withMetadata` | object | No |  |
| `withZeroValue` | boolean | No | value 0 result parameter . parameter true . Default: `False`. |
| `withFunction` | boolean | No | function parameter . parameter true input , . Default: `False`. |


## Response

### Success (200) - Successful Response

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

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
