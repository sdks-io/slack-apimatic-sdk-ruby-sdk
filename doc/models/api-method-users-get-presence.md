
# Api Method Users Get Presence

Generated from users.getPresence with shasum e7251aec575d8863f9e0eb38663ae9dc26655f65

*This model accepts additional fields of type Object.*

## Structure

`ApiMethodUsersGetPresence`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto_away` | `TrueClass \| FalseClass` | Optional | - |
| `connection_count` | `Integer` | Optional | - |
| `last_activity` | `Integer` | Optional | - |
| `manual_away` | `TrueClass \| FalseClass` | Optional | - |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `online` | `TrueClass \| FalseClass` | Optional | - |
| `presence` | `String` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "ok": "True",
  "presence": "presence8",
  "auto_away": false,
  "connection_count": 42,
  "last_activity": 166,
  "manual_away": false,
  "online": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

