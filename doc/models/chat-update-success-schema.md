
# Chat Update Success Schema

Schema for successful response of chat.update method

*This model accepts additional fields of type Object.*

## Structure

`ChatUpdateSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `String` | Required | - |
| `message` | [`MessageObject1`](../../doc/models/message-object-1.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `text` | `String` | Required | - |
| `ts` | `String` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "channel": "channel8",
  "message": {
    "attachments": [
      {
        "key1": "val1",
        "key2": "val2"
      },
      {
        "key1": "val1",
        "key2": "val2"
      }
    ],
    "blocks": {
      "key1": "val1",
      "key2": "val2"
    },
    "text": "text0",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "ok": "True",
  "text": "text6",
  "ts": "ts8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

