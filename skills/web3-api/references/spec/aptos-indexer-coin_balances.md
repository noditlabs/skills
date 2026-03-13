# coin_balances

> Query historical coin balance snapshots on Aptos. Each record represents a balance at a specific transaction version.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `amount` | numeric | Coin balance amount |
| `coin_type` | String | Full coin type identifier |
| `coin_type_hash` | String | Hash of the coin type |
| `owner_address` | String | Address of the coin owner |
| `transaction_timestamp` | timestamp | Timestamp of the balance snapshot |
| `transaction_version` | bigint | Transaction version number |

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
query GetCoinBalances {
  coin_balances(
    where: {
      owner_address: { _eq: "0x1" }
      coin_type: { _eq: "0x1::aptos_coin::AptosCoin" }
    }
    order_by: { transaction_version: desc }
    limit: 10
  ) {
    amount
    coin_type
    owner_address
    transaction_timestamp
    transaction_version
  }
}
```
