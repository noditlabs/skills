# move_resources

> Query Move resources on the Aptos blockchain. Returns address and transaction version pairs for Move resource changes.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `address` | String | The account address that holds the resource |
| `transaction_version` | bigint | Transaction version number when the resource was modified |

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
query GetMoveResources {
  move_resources(
    where: { address: { _eq: "0x1" } }
    order_by: { transaction_version: desc }
    limit: 10
  ) {
    address
    transaction_version
  }
}
```
