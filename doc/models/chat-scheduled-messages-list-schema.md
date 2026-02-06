
# Chat Scheduled Messages List Schema

Schema for successful response from chat.scheduledMessages.list method

*This model accepts additional fields of type Object.*

## Structure

`ChatScheduledMessagesListSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `response_metadata` | [`ResponseMetadata`](../../doc/models/response-metadata.md) | Required | - |
| `scheduled_messages` | [`Array[ScheduledMessage]`](../../doc/models/scheduled-message.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "ok": "True",
  "response_metadata": {
    "next_cursor": "next_cursor2",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "scheduled_messages": [
    {
      "channel_id": "channel_id8",
      "date_created": 100,
      "id": "id2",
      "post_at": 0,
      "text": "text2",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

