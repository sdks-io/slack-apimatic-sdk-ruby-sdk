
# Conversations Open Success Schema

Schema for successful response from conversations.open method when opening channels, ims, mpims

*This model accepts additional fields of type Object.*

## Structure

`ConversationsOpenSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `already_open` | `TrueClass \| FalseClass` | Optional | - |
| `channel` | `Object` | Required | - |
| `no_op` | `TrueClass \| FalseClass` | Optional | - |
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
  "already_open": false,
  "no_op": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

