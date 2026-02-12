
# Conversations Close Error Schema Exception

Schema for error response from conversations.close method

*This model accepts additional fields of type Object.*

## Structure

`ConversationsCloseErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `callstack` | `String` | Optional | Note: PHP callstack is only visible in dev/qa |
| `error` | [`ConversationsCloseErrorEnum`](../../doc/models/conversations-close-error-enum.md) | Required | - |
| `needed` | `String` | Optional | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `provided` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "invalid_json",
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

