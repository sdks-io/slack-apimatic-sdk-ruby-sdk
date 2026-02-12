
# Users Info Error Schema Exception

Schema for error response from users.info method

*This model accepts additional fields of type Object.*

## Structure

`UsersInfoErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `callstack` | `String` | Optional | - |
| `error` | [`UsersInfoErrorEnum`](../../doc/models/users-info-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "not_authed",
  "ok": "False",
  "callstack": "callstack4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

