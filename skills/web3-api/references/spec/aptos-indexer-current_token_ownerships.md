# current_token_ownerships

> Query the current (latest) token ownership state on Aptos. Shows which addresses currently own which tokens and in what amounts.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `amount` | numeric | Number of tokens owned |
| `collection_data_id_hash` | String | Hash of the parent collection |
| `collection_name` | String | Name of the parent collection |
| `creator_address` | String | Address of the token creator |
| `last_transaction_timestamp` | timestamp | Timestamp of the last ownership change |
| `last_transaction_version` | bigint | Version of the last ownership change |
| `name` | String | Token name |
| `owner_address` | String | Address of the current owner |
| `property_version` | numeric | Property version of the token |
| `table_type` | String | Type of the storage table |
| `token_data_id_hash` | String | Unique hash of the token data |
| `token_properties` | jsonb | Token properties |

## Relationships

### Object Relationships

| Relationship | Remote Table | Join On |
|-------------|-------------|---------|
| `aptos_name` | current_aptos_names | `name` = `token_name` |
| `current_collection_data` | current_collection_datas | `collection_data_id_hash` = `collection_data_id_hash` |
| `current_token_data` | current_token_datas | `token_data_id_hash` = `token_data_id_hash` |

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
query GetCurrentTokenOwnerships {
  current_token_ownerships(
    where: {
      owner_address: { _eq: "0x1" }
      amount: { _gt: "0" }
    }
    order_by: { last_transaction_version: desc }
    limit: 20
  ) {
    collection_name
    name
    amount
    owner_address
    property_version
    last_transaction_timestamp
    current_token_data {
      metadata_uri
      description
    }
    current_collection_data {
      supply
      maximum
    }
  }
}
```
