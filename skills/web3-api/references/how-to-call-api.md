# How to Call API

How to call the Nodit API. Base URL, authentication, and request format differ by API type.

## Authentication

`X-API-KEY` header is required for all APIs.

```
X-API-KEY: {api_key}
```

API Keys are issued after signing up at https://nodit.lambda256.io.

## Data API

Query indexed blockchain data. POST request, JSON body.

```
POST https://web3.nodit.io/{chain}/{network}/{category}/{operationId}

Headers:
  X-API-KEY: {api_key}
  Content-Type: application/json

Body:
  {Parameters by operationId — see references/{operationId}.md}
```

**Example** — List of tokens held by an Ethereum account:
```
POST https://web3.nodit.io/ethereum/mainnet/token/getTokensOwnedByAccount

{"accountAddress": "0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045"}
```

## Node API

Direct requests to blockchain nodes via JSON-RPC. POST request.

```
POST https://{chain}-{network}.nodit.io

Headers:
  X-API-KEY: {api_key}
  Content-Type: application/json

Body:
  {"jsonrpc": "2.0", "id": 1, "method": "{method}", "params": [...]}
```

**Example** — Query Ethereum account balance:
```
POST https://ethereum-mainnet.nodit.io

{"jsonrpc": "2.0", "id": 1, "method": "eth_getBalance", "params": ["0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045", "latest"]}
```

**operationId → method mapping:**
- Ethereum: operationId is the method itself (`eth_getBalance`)
- Other chains: Remove `{chain}-` prefix from operationId → method (`polygon-eth_getBalance` → `eth_getBalance`)

## Aptos Indexer API

Query Aptos indexed data via GraphQL. POST request.

```
POST https://aptos-{network}.nodit.io/v1/graphql

Headers:
  X-API-KEY: {api_key}
  Content-Type: application/json

Body:
  {"query": "{GraphQL query}", "variables": {}}
```

**Example** — Coin balance of an account:
```
POST https://aptos-mainnet.nodit.io/v1/graphql

{"query": "{ current_coin_balances(where: {owner_address: {_eq: \"0x1\"}}) { coin_type amount coin_info { name symbol decimals } } }"}
```

**Filtering:** Hasura style — `_eq`, `_gt`, `_lt`, `_in`, `_is_null`, etc. `order_by`, `limit`, `offset` supported.

## Webhook API

Manage on-chain event subscriptions. REST API.

```
Base URL: https://web3.nodit.io/v1/{chain}/{network}/webhooks

Headers:
  X-API-KEY: {api_key}
  Content-Type: application/json
```

| Action | Method | Path |
|--------|--------|------|
| Create | POST | `/` |
| Get | GET | `/{subscriptionId}` |
| Update | PUT | `/{subscriptionId}` |
| Delete | DELETE | `/{subscriptionId}` |
| History | GET | `/{subscriptionId}/history` |

## chain / network Values

For the chain and network strings used in API calls, refer to `supported-chains.md`.

| chain value | network value |
|-------------|---------------|
| ethereum | mainnet, sepolia, hoodi |
| arbitrum | mainnet, sepolia |
| base | mainnet, sepolia |
| optimism | mainnet, sepolia |
| polygon | mainnet, amoy |
| bnb | mainnet, testnet |
| kaia | mainnet, kairos |
| luniverse | mainnet |
| giwa | sepolia |
| arc | testnet |
| chiliz | mainnet |
| ethereumclassic | mainnet |
| solana | mainnet, devnet |
| sui | mainnet |
| aptos | mainnet, testnet |
| bitcoin | mainnet |
| bitcoincash | mainnet |
| dogecoin | mainnet |
| tron | mainnet |
| xrpl | mainnet |
