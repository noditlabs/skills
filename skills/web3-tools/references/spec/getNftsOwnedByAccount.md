# getNftsOwnedByAccount

> Get NFTs Owned By Account

- **Category**: Data API - NFT

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

`POST /{chain}/{network}/nft/getNftsOwnedByAccount`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `chain` | string | Yes | Parameter to specify the target chain. Enum: `arbitrum`, `arc`, `base`, `bnb`, `chiliz`, `ethereum`, `ethereumclassic`, `giwa`, `kaia`, `luniverse`, `optimism`, `polygon`. Default: `arbitrum`. |
| `network` | string | Yes | Parameter to specify the target network of the chain. Supported networks may vary by chain. Enum: `mainnet`, `sepolia`, `testnet`, `hoodi`, `kairos`, `amoy`. Default: `mainnet`. |

### Headers

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `X-API-KEY` | string | Yes | API key from Nodit console. Use environment variable: `$NODIT_API_KEY` |

## Request Body

`Content-Type: application/json`

### Arbitrum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |

### Arc

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |

### Base

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |

### BNB Smart Chain

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |

### Chiliz

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |

### Ethereum

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |

### Ethereum Classic

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |

### Giwa

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |

### Kaia

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |

### Luniverse

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |

### Optimism

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |

### Polygon

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `accountAddress` | string | Yes | address parameter . 0x 40 hexadecimal string input . |
| `contractAddresses` | object | No |  |
| `page` | integer | No | page parameter data . parameter 100 value , 100 cursor . page parameter cursor parameter . page cursor value input , cursor . |
| `rpp` | integer | No | rpp results per page , parameter . 0 1000 . |
| `cursor` | string | No | cursor parameter parameter , data . cursor value data . page parameter cursor parameter . page cursor value input , cursor . |
| `withCount` | boolean | No | count parameter , count data . parameter true input , count . Default: `False`. |
| `withMetadata` | boolean | No | NFT token data (rawMetadata, metadataSyncedAt) parameter . parameter true input , . Default: `False`. |


## Response

### Success (200) - Successful Response

**Arbitrum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (Arbitrum):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

**Arc:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (Arc):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

**Base:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (Base):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

**BNB Smart Chain:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (BNB Smart Chain):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

**Chiliz:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (Chiliz):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

**Ethereum:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (Ethereum):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

**Ethereum Classic:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (Ethereum Classic):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

**Giwa:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (Giwa):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

**Kaia:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (Kaia):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

**Luniverse:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (Luniverse):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

**Optimism:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (Optimism):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

**Polygon:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `page` | integer | No | page parameter number field. page parameter 0 value input . |
| `rpp` | integer | No | rpp parameter result field. |
| `cursor` | string | No | cursor , data value. |
| `count` | integer | No | data field. withCount parameter true input . |

**Items Schema (Polygon):**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `ownerAddress` | string | Yes | address field. |
| `balance` | string | Yes | 잔고 나타내는 필드입니다. |
| `lastTransferredAt` | string | Yes | token NFT ISO 8601 . token (ERC20, ERC721, ERC1155) Transfer event , event . |
| `tokenId` | string | Yes | NFT token ID field. ID NFT . |
| `tokenUri` | string | Yes | NFT data URI. contract , IPFS address URL . |
| `tokenUriSyncedAt` | string | Yes | NFT tokenUri field. |
| `rawMetadata` | string | No | NFT rawMetadata field. withMetadata parameter true input . |
| `metadataSyncedAt` | string | No | NFT metadata field. withMetadata parameter true input . |
| `contract` | object | No |  |

### Error Responses

| Status | Code | Description |
|--------|------|-------------|
| 400 | `INVALID_PARAMETER` | Invalid parameter provided |
| 401 | `AUTHENTICATION_FAILED` | Authentication failed |
| 403 | `PERMISSION_DENIED` | Permission denied |
| 404 | `RESOURCE_NOT_FOUND` | Resource not found |
| 429 | `TOO_MANY_REQUESTS` | Too many requests |
