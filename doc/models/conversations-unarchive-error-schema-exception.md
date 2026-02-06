
# Conversations Unarchive Error Schema Exception

Schema for error response from conversations.unarchive method

*This model accepts additional fields of type Object.*

## Structure

`ConversationsUnarchiveErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `callstack` | `String` | Optional | Note: PHP callstack is only visible in dev/qa |
| `error` | [`Error48`](../../doc/models/error-48.md) | Required | - |
| `needed` | `String` | Optional | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `provided` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "invalid_form_data",
  "ok": "False",
  "callstack": "callstack2",
  "needed": "needed6",
  "provided": "provided2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

