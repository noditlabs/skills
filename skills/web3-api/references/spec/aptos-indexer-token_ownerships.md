# token_ownerships

> Query historical token ownership records on Aptos. Each record represents an ownership state at a specific transaction version.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `amount` | numeric | Number of tokens owned at this version |
| `collection_data_id_hash` | String | Hash of the parent collection |
| `collection_name` | String | Name of the parent collection |
| `creator_address` | String | Address of the token creator |
| `name` | String | Token name |
| `owner_address` | String | Address of the owner at this version |
| `property_version` | numeric | Property version of the token |
| `table_handle` | String | Storage table handle |
| `table_type` | String | Type of the storage table |
| `token_data_id_hash` | String | Unique hash of the token data |
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
query GetTokenOwnerships {
  token_ownerships(
    where: {
      owner_address: { _eq: "0x1" }
      amount: { _gt: "0" }
    }
    order_by: { transaction_version: desc }
    limit: 20
  ) {
    collection_name
    name
    amount
    owner_address
    property_version
    transaction_timestamp
    transaction_version
  }
}
```
