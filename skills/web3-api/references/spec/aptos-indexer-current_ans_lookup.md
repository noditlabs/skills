# current_ans_lookup

> Query the current state of Aptos Name Service (ANS) lookups. Maps domain/subdomain names to registered addresses.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `domain` | String | Primary domain name |
| `expiration_timestamp` | timestamp | When the name registration expires |
| `is_deleted` | Boolean | Whether the name has been deleted |
| `last_transaction_version` | bigint | Last transaction version that modified this record |
| `registered_address` | String | Address registered to this name |
| `subdomain` | String | Subdomain name (empty string if none) |
| `token_name` | String | Associated token name |

## Relationships

### Array Relationships

| Relationship | Remote Table | Join On |
|-------------|-------------|---------|
| `all_token_ownerships` | current_token_ownerships | `token_name` = `name` |

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
query GetANSLookup {
  current_ans_lookup(
    where: {
      registered_address: { _eq: "0x1" }
      is_deleted: { _eq: false }
    }
    limit: 10
  ) {
    domain
    subdomain
    registered_address
    expiration_timestamp
    token_name
  }
}
```
