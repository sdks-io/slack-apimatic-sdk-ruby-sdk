
# Users Identity Error Schema Exception

Schema for error response from users.identity method

*This model accepts additional fields of type Object.*

## Structure

`UsersIdentityErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `callstack` | `String` | Optional | Note: PHP callstack is only visible in dev/qa |
| `error` | [`Error12`](../../doc/models/error-12.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "invalid_charset",
  "ok": "False",
  "callstack": "callstack6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

