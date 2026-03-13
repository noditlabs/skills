# address_version_from_move_resources

> Query address-version pairs derived from Move resources on the Aptos blockchain. Useful for mapping addresses to their transaction versions.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `address` | String | The account address associated with the Move resource |
| `transaction_version` | bigint | The transaction version number |

## Relationships

### Array Relationships

| Relationship | Remote Table | Join On | Description |
|-------------|-------------|---------|-------------|
| `coin_activities` | coin_activities | `transaction_version` = `transaction_version` | Coin activities at this transaction version |
| `delegated_staking_activities` | delegated_staking_activities | `transaction_version` = `transaction_version` | Delegated staking activities at this version |
| `token_activities` | token_activities | `transaction_version` = `transaction_version` | Token activities at this version |
| `token_activities_v2` | token_activities_v2 | `transaction_version` = `transaction_version` | Token activities v2 at this version |

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
query GetAddressVersions {
  address_version_from_move_resources(
    where: { address: { _eq: "0x1" } }
    order_by: { transaction_version: desc }
    limit: 10
  ) {
    address
    transaction_version
    coin_activities {
      activity_type
      amount
      coin_type
    }
  }
}
```
