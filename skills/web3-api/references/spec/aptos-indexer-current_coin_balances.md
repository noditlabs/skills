# current_coin_balances

> Query the current (latest) coin balances for accounts on Aptos. Returns the most up-to-date balance for each coin type held by an address.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `amount` | numeric | Current coin balance amount |
| `coin_type` | String | Full coin type identifier |
| `coin_type_hash` | String | Hash of the coin type |
| `last_transaction_timestamp` | timestamp | Timestamp of the last balance-changing transaction |
| `last_transaction_version` | bigint | Version of the last balance-changing transaction |
| `owner_address` | String | Address of the coin owner |

## Relationships

### Object Relationships

| Relationship | Remote Table | Join On |
|-------------|-------------|---------|
| `coin_info` | coin_infos | `coin_type_hash` = `coin_type_hash` |

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
query GetCurrentCoinBalances {
  current_coin_balances(
    where: { owner_address: { _eq: "0x1" } }
    order_by: { amount: desc }
  ) {
    amount
    coin_type
    last_transaction_timestamp
    owner_address
    coin_info {
      name
      symbol
      decimals
    }
  }
}
```
