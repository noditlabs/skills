# tokens

> Query token instances on Aptos. Each record represents a specific token with its properties at a given transaction version.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `collection_data_id_hash` | String | Hash of the parent collection |
| `collection_name` | String | Name of the parent collection |
| `creator_address` | String | Address of the token creator |
| `name` | String | Token name |
| `property_version` | numeric | Property version of the token |
| `token_data_id_hash` | String | Unique hash of the token data |
| `token_properties` | jsonb | Token properties (key-value pairs) |
| `transaction_timestamp` | timestamp | Timestamp of the transaction |
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
query GetTokens {
  tokens(
    where: {
      collection_name: { _eq: "Aptos Monkeys" }
      creator_address: { _eq: "0x1" }
    }
    order_by: { transaction_version: desc }
    limit: 10
  ) {
    name
    collection_name
    creator_address
    property_version
    token_properties
    transaction_timestamp
    transaction_version
  }
}
```
