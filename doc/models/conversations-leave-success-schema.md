
# Conversations Leave Success Schema

Schema for successful response from conversations.leave method

*This model accepts additional fields of type Object.*

## Structure

`ConversationsLeaveSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `not_in_channel` | `TrueClass \| FalseClass` | Optional | - |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "ok": "True",
  "not_in_channel": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

