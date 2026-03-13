# current_token_datas

> Query the current (latest) state of individual NFT/token data on Aptos, including metadata, royalty info, and mutability settings.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `collection_data_id_hash` | String | Hash of the parent collection |
| `collection_name` | String | Name of the parent collection |
| `creator_address` | String | Address of the token creator |
| `default_properties` | jsonb | Default token properties |
| `description` | String | Token description |
| `description_mutable` | Boolean | Whether description can be changed |
| `largest_property_version` | numeric | Largest property version |
| `last_transaction_timestamp` | timestamp | Timestamp of the last modifying transaction |
| `last_transaction_version` | bigint | Version of the last modifying transaction |
| `maximum` | numeric | Maximum supply of this token |
| `maximum_mutable` | Boolean | Whether maximum can be changed |
| `metadata_uri` | String | URI for token metadata |
| `name` | String | Token name |
| `payee_address` | String | Address that receives royalties |
| `properties_mutable` | Boolean | Whether properties can be changed |
| `royalty_mutable` | Boolean | Whether royalty settings can be changed |
| `royalty_points_denominator` | numeric | Royalty fraction denominator |
| `royalty_points_numerator` | numeric | Royalty fraction numerator |
| `supply` | numeric | Current supply |
| `token_data_id_hash` | String | Unique hash identifier for the token data |
| `uri_mutable` | Boolean | Whether URI can be changed |

## Relationships

### Object Relationships

| Relationship | Remote Table | Join On |
|-------------|-------------|---------|
| `current_collection_data` | current_collection_datas | `collection_data_id_hash` = `collection_data_id_hash` |

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
query GetCurrentTokenDatas {
  current_token_datas(
    where: {
      collection_name: { _eq: "Aptos Monkeys" }
      creator_address: { _eq: "0x1" }
    }
    order_by: { last_transaction_version: desc }
    limit: 10
  ) {
    name
    description
    metadata_uri
    supply
    maximum
    royalty_points_numerator
    royalty_points_denominator
    payee_address
    current_collection_data {
      collection_name
      supply
    }
  }
}
```
