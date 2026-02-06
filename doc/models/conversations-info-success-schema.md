
# Conversations Info Success Schema

Schema for successful response conversations.info

*This model accepts additional fields of type Object.*

## Structure

`ConversationsInfoSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `Object` | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "channel": {
    "key1": "val1",
    "key2": "val2"
  },
  "ok": "True",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

