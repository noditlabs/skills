# collection_datas

> Query historical NFT collection data on Aptos. Each record represents a collection state at a specific transaction version.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `collection_data_id_hash` | String | Unique hash identifier for the collection |
| `collection_name` | String | Name of the collection |
| `creator_address` | String | Address of the collection creator |
| `description` | String | Collection description |
| `description_mutable` | Boolean | Whether description can be changed |
| `maximum` | numeric | Maximum number of tokens in the collection |
| `maximum_mutable` | Boolean | Whether maximum can be changed |
| `metadata_uri` | String | URI for collection metadata |
| `supply` | numeric | Current supply of tokens |
| `table_handle` | String | Table handle for the collection |
| `transaction_timestamp` | timestamp | Timestamp of the transaction |
| `transaction_version` | bigint | Transaction version number |
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
query GetCollectionDatas {
  collection_datas(
    where: { creator_address: { _eq: "0x1" } }
    order_by: { transaction_version: desc }
    limit: 10
  ) {
    collection_name
    creator_address
    description
    maximum
    supply
    metadata_uri
    transaction_timestamp
  }
}
```
