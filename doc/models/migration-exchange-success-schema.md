
# Migration Exchange Success Schema

Schema for successful response from migration.exchange method

*This model accepts additional fields of type Object.*

## Structure

`MigrationExchangeSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enterprise_id` | `String` | Required | - |
| `invalid_user_ids` | `Array[String]` | Optional | - |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `team_id` | `String` | Required | **Constraints**: *Pattern*: `^[T][A-Z0-9]{2,}$` |
| `user_id_map` | `Object` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "enterprise_id": "enterprise_id8",
  "ok": "True",
  "team_id": "team_id8",
  "invalid_user_ids": [
    "invalid_user_ids6"
  ],
  "user_id_map": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

