
# Auth Test Success Schema

Schema for successful response auth.test method

*This model accepts additional fields of type Object.*

## Structure

`AuthTestSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `bot_id` | `String` | Optional | **Constraints**: *Pattern*: `^B[A-Z0-9]{8,}$` |
| `is_enterprise_install` | `TrueClass \| FalseClass` | Optional | - |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `team` | `String` | Required | - |
| `team_id` | `String` | Required | **Constraints**: *Pattern*: `^[T][A-Z0-9]{2,}$` |
| `url` | `String` | Required | - |
| `user` | `String` | Required | - |
| `user_id` | `String` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "ok": "True",
  "team": "team0",
  "team_id": "team_id4",
  "url": "url4",
  "user": "user0",
  "user_id": "user_id8",
  "bot_id": "bot_id6",
  "is_enterprise_install": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

