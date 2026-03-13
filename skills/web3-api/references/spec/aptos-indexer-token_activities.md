# token_activities

> Query historical NFT/token activity events on Aptos, including transfers, mints, burns, offers, and claims.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `coin_amount` | numeric | Amount of coin involved (if applicable) |
| `coin_type` | String | Coin type used in the activity |
| `collection_data_id_hash` | String | Hash of the parent collection |
| `collection_name` | String | Name of the parent collection |
| `creator_address` | String | Address of the token creator |
| `event_account_address` | String | Address of the account that emitted the event |
| `event_creation_number` | bigint | Event creation number |
| `event_index` | bigint | Index of the event within the transaction |
| `event_sequence_number` | bigint | Sequence number of the event |
| `from_address` | String | Sender address |
| `name` | String | Token name |
| `property_version` | numeric | Property version of the token |
| `to_address` | String | Receiver address |
| `token_amount` | numeric | Number of tokens transferred |
| `token_data_id_hash` | String | Unique hash of the token data |
| `transaction_timestamp` | timestamp | Timestamp of the transaction |
| `transaction_version` | bigint | Transaction version number |
| `transfer_type` | String | Type of transfer activity |

## Relationships

### Object Relationships

| Relationship | Remote Table | Join On |
|-------------|-------------|---------|
| `current_token_data` | current_token_datas | `token_data_id_hash` = `token_data_id_hash` |

### Array Relationships

| Relationship | Remote Table | Join On |
|-------------|-------------|---------|
| `aptos_names_owner` | current_aptos_names | `event_account_address` = `registered_address` |
| `aptos_names_to` | current_aptos_names | `to_address` = `registered_address` |

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
query GetTokenActivities {
  token_activities(
    where: {
      collection_name: { _eq: "Aptos Monkeys" }
    }
    order_by: { transaction_version: desc }
    limit: 20
  ) {
    transfer_type
    from_address
    to_address
    name
    token_amount
    transaction_timestamp
    transaction_version
    current_token_data {
      metadata_uri
    }
  }
}
```
