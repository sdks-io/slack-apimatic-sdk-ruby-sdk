
# Auth Test Error Schema Exception

Schema for error response auth.test method

*This model accepts additional fields of type Object.*

## Structure

`AuthTestErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `callstack` | `String` | Optional | Note: PHP callstack is only visible in dev/qa |
| `error` | [`AuthTestErrorEnum`](../../doc/models/auth-test-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "invalid_charset",
  "ok": "False",
  "callstack": "callstack0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

