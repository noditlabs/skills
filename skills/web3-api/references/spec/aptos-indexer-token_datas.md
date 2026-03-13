# token_datas

> Query historical NFT/token data on Aptos. Each record represents the token data state at a specific transaction version.

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
| `maximum` | numeric | Maximum supply of this token |
| `maximum_mutable` | Boolean | Whether maximum can be changed |
| `metadata_uri` | String | URI for token metadata |
| `name` | String | Token name |
| `payee_address` | String | Address that receives royalties |
| `properties_mutable` | Boolean | Whether properties can be changed |
| `royalty_mutable` | Boolean | Whether royalty settings can be changed |
| `royalty_points_denominator` | numeric | Royalty fraction denominator |
| `royalty_points_numerator` | numeric | Royalty fraction numerator |
| `supply` | numeric | Current supply at this version |
| `token_data_id_hash` | String | Unique hash identifier for the token data |
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
query GetTokenDatas {
  token_datas(
    where: {
      creator_address: { _eq: "0x1" }
      collection_name: { _eq: "Aptos Monkeys" }
    }
    order_by: { transaction_version: desc }
    limit: 10
  ) {
    name
    description
    metadata_uri
    supply
    maximum
    royalty_points_numerator
    royalty_points_denominator
    transaction_timestamp
    transaction_version
  }
}
```
