
# Conversations List Success Schema

Schema for successful response from conversations.list method

*This model accepts additional fields of type Object.*

## Structure

`ConversationsListSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channels` | `Array[Object]` | Required | **Constraints**: *Unique Items Required* |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `response_metadata` | [`ResponseMetadata`](../../doc/models/response-metadata.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "channels": [
    {
      "key1": "val1",
      "key2": "val2"
    },
    {
      "key1": "val1",
      "key2": "val2"
    }
  ],
  "ok": "True",
  "response_metadata": {
    "next_cursor": "next_cursor2",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

