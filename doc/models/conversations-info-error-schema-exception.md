
# Conversations Info Error Schema Exception

Schema for error response from conversations.info method

*This model accepts additional fields of type Object.*

## Structure

`ConversationsInfoErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `callstack` | `String` | Optional | Note: PHP callstack is only visible in dev/qa |
| `error` | [`Error34`](../../doc/models/error-34.md) | Required | - |
| `needed` | `String` | Optional | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `provided` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "team_added_to_org",
  "ok": "False",
  "callstack": "callstack8",
  "needed": "needed8",
  "provided": "provided8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

