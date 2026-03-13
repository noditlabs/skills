# coin_activities

> Query historical coin (fungible token) activity events on Aptos, including transfers, mints, burns, and gas fees.

- **Category**: Aptos Indexer API (GraphQL)

## Fields

| Field | Type | Description |
|-------|------|-------------|
| `activity_type` | String | Type of activity (e.g., transfer, mint, burn) |
| `amount` | numeric | Amount of coins involved |
| `block_height` | bigint | Block height of the transaction |
| `coin_type` | String | Full coin type identifier (e.g., `0x1::aptos_coin::AptosCoin`) |
| `entry_function_id_str` | String | Entry function identifier string |
| `event_account_address` | String | Address of the account that emitted the event |
| `event_creation_number` | bigint | Event creation number |
| `event_index` | bigint | Index of the event within the transaction |
| `event_sequence_number` | bigint | Sequence number of the event |
| `is_gas_fee` | Boolean | Whether this activity is a gas fee payment |
| `is_transaction_success` | Boolean | Whether the parent transaction succeeded |
| `owner_address` | String | Address of the coin owner |
| `storage_refund_amount` | numeric | Storage refund amount |
| `transaction_timestamp` | timestamp | Timestamp of the transaction |
| `transaction_version` | bigint | Transaction version number |

## Relationships

### Object Relationships

| Relationship | Remote Table | Join On |
|-------------|-------------|---------|
| `coin_info` | coin_infos | `coin_type` = `coin_type` |

### Array Relationships

| Relationship | Remote Table | Join On |
|-------------|-------------|---------|
| `aptos_names` | current_aptos_names | `owner_address` = `registered_address` |

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
query GetCoinActivities {
  coin_activities(
    where: {
      owner_address: { _eq: "0x1" }
      coin_type: { _eq: "0x1::aptos_coin::AptosCoin" }
    }
    order_by: { transaction_version: desc }
    limit: 20
  ) {
    activity_type
    amount
    block_height
    coin_type
    is_gas_fee
    is_transaction_success
    transaction_timestamp
    transaction_version
    coin_info {
      name
      symbol
      decimals
    }
  }
}
```
