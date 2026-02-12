
# Conversations Mark Error Schema Exception

Schema for error response from conversations.mark method

*This model accepts additional fields of type Object.*

## Structure

`ConversationsMarkErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `callstack` | `String` | Optional | Note: PHP callstack is only visible in dev/qa |
| `error` | [`ConversationsMarkErrorEnum`](../../doc/models/conversations-mark-error-enum.md) | Required | - |
| `needed` | `String` | Optional | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `provided` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "not_allowed_token_type",
  "ok": "False",
  "callstack": "callstack4",
  "needed": "needed2",
  "provided": "provided4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

