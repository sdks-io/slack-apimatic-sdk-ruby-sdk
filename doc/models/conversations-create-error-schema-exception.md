
# Conversations Create Error Schema Exception

Schema for error response from conversations.create method

*This model accepts additional fields of type Object.*

## Structure

`ConversationsCreateErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `callstack` | `String` | Optional | Note: PHP callstack is only visible in dev/qa |
| `detail` | `String` | Optional | - |
| `error` | [`ConversationsCreateErrorEnum`](../../doc/models/conversations-create-error-enum.md) | Required | - |
| `needed` | `String` | Optional | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `provided` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "invalid_array_arg",
  "ok": "False",
  "callstack": "callstack0",
  "detail": "detail4",
  "needed": "needed4",
  "provided": "provided0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

