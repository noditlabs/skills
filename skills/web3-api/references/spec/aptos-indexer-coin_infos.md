# coin_infos

> Query metadata about coins (fungible tokens) registered on Aptos, including name, symbol, decimals, and creator information.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `coin_type` | String | Full coin type identifier (e.g., `0x1::aptos_coin::AptosCoin`) |
| `coin_type_hash` | String | Hash of the coin type |
| `creator_address` | String | Address of the coin creator |
| `decimals` | integer | Number of decimal places |
| `name` | String | Human-readable coin name |
| `supply_aggregator_table_handle` | String | Table handle for supply aggregator |
| `supply_aggregator_table_key` | String | Table key for supply aggregator |
| `symbol` | String | Coin ticker symbol |
| `transaction_created_timestamp` | timestamp | When the coin was created |
| `transaction_version_created` | bigint | Transaction version when coin was created |

## Relationships

None.

## Arguments / Filters

Standard Hasura filters apply to all columns:

- `_eq`, `_neq` - equality / inequality
- `_gt`, `_gte`, `_lt`, `_lte` - comparison operators
- `_in`, `_nin` - set membership
- `_is_null` - null check
- `order_by` - sort by any column (asc/desc)
- `limit` / `offset` - pagination
- `where` - composite filter object

## Example Query

```graphql
query GetCoinInfos {
  coin_infos(
    where: { symbol: { _eq: "APT" } }
    limit: 10
  ) {
    coin_type
    creator_address
    decimals
    name
    symbol
    transaction_created_timestamp
  }
}
```
