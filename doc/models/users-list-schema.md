
# Users List Schema

Schema for successful response from users.list method

*This model accepts additional fields of type Object.*

## Structure

`UsersListSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cache_ts` | `Integer` | Required | - |
| `members` | `Array[Object]` | Required | **Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `response_metadata` | `Object` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "cache_ts": 154,
  "members": [
    {
      "key1": "val1",
      "key2": "val2"
    },
    {
      "key1": "val1",
      "key2": "val2"
    }
  ],
  "ok": "True",
  "response_metadata": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

