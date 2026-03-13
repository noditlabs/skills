# getTransactionByHash

> Retrieves detailed information about a specific transaction using its hash.

- **Category**: Data API
- **Official Docs**: https://developer.nodit.io/reference/getTransactionByHash

## Supported Chains
- arbitrum, base, bnb, chiliz, ethereum, ethereumclassic, giwa, kaia, optimism, polygon, luniverse, xrpl, aptos
- **Networks**: mainnet, testnet, sepolia, hoodi, amoy

## Endpoint
`POST /{chain}/{network}/blockchain/getTransactionByHash`

## Parameters

### Path Parameters

| Name | Type | Required | Description |
|------|------|----------|-------------|
| chain | string | Yes | Target chain |
| network | string | Yes | Target network |

## Request Body

Schema varies by chain (oneOf):

**EVM chains:**

| Name | Type | Required | Description |
|------|------|----------|-------------|
| transactionHash | string | Yes | Transaction hash (0x-prefixed 64 hex characters) |
| withLogs | boolean | No | Include event logs in response |
| withDecode | boolean | No | Include decoded data in response |

**XRPL:**

| Name | Type | Required | Description |
|------|------|----------|-------------|
| transactionHash | string | Yes | Transaction hash (64 hex characters) |
| withBalanceChanges | boolean | No | Include balance changes in response |
| withTokenTransfers | boolean | No | Include token transfer details |

**Aptos:**

| Name | Type | Required | Description |
|------|------|----------|-------------|
| transactionHash | string | Yes | Transaction hash (0x-prefixed 64 hex characters) |
| withBalanceChanges | boolean | No | Include balance changes in response |

## Response

Response schema varies by chain. Common fields include transaction hash, block height, block timestamp, sender, status, gas used, and chain-specific transaction details.
