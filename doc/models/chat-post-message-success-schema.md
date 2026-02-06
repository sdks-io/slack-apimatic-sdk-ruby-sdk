
# Chat Post Message Success Schema

Schema for successful response of chat.postMessage method

*This model accepts additional fields of type Object.*

## Structure

`ChatPostMessageSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `String` | Required | **Constraints**: *Pattern*: `^[CGD][A-Z0-9]{8,}$` |
| `message` | [`MessageObject`](../../doc/models/message-object.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `ts` | `String` | Required | **Constraints**: *Pattern*: `^\d{10}\.\d{6}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "channel": "channel6",
  "message": {
    "attachments": [
      {
        "fallback": "fallback4",
        "id": 36,
        "image_bytes": 34,
        "image_height": 154,
        "image_url": "image_url6",
        "image_width": 24,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "fallback": "fallback4",
        "id": 36,
        "image_bytes": 34,
        "image_height": 154,
        "image_url": "image_url6",
        "image_width": 24,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
    "blocks": [
      {
        "type": "type4",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "type": "type4",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
    "bot_id": {
      "key1": "val1",
      "key2": "val2"
    },
    "bot_profile": {
      "app_id": "app_id8",
      "deleted": false,
      "icons": {
        "image_36": "image_362",
        "image_48": "image_488",
        "image_72": "image_722",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "id": "id8",
      "name": "name8",
      "team_id": "team_id8",
      "updated": 44,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "client_msg_id": "client_msg_id4",
    "text": "text0",
    "ts": "ts2",
    "type": "type0",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "ok": "True",
  "ts": "ts0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

