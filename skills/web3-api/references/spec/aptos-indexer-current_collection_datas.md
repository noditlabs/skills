# current_collection_datas

> Query the current (latest) state of NFT collections on Aptos. Returns the most up-to-date collection metadata.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `collection_data_id_hash` | String | Unique hash identifier for the collection |
| `collection_name` | String | Name of the collection |
| `creator_address` | String | Address of the collection creator |
| `description` | String | Collection description |
| `description_mutable` | Boolean | Whether description can be changed |
| `last_transaction_timestamp` | timestamp | Timestamp of the last modifying transaction |
| `last_transaction_version` | bigint | Version of the last modifying transaction |
| `maximum` | numeric | Maximum number of tokens in the collection |
| `maximum_mutable` | Boolean | Whether maximum can be changed |
| `metadata_uri` | String | URI for collection metadata |
| `supply` | numeric | Current supply of tokens |
| `table_handle` | String | Table handle for the collection |
| `uri_mutable` | Boolean | Whether URI can be changed |

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
query GetCurrentCollections {
  current_collection_datas(
    where: { creator_address: { _eq: "0x1" } }
    order_by: { last_transaction_version: desc }
    limit: 10
  ) {
    collection_name
    creator_address
    description
    maximum
    supply
    metadata_uri
    last_transaction_timestamp
  }
}
```
