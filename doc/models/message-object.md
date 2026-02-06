
# Message Object

*This model accepts additional fields of type Object.*

## Structure

`MessageObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `attachments` | [`Array[Attachment]`](../../doc/models/attachment.md) | Optional | **Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `blocks` | [`Array[BlockKitBlock]`](../../doc/models/block-kit-block.md) | Optional | This is a very loose definition, in the future, we'll populate this with deeper schema in this definition namespace. |
| `bot_id` | `Object` | Optional | - |
| `bot_profile` | [`BotProfileObject`](../../doc/models/bot-profile-object.md) | Optional | - |
| `client_msg_id` | `String` | Optional | - |
| `comment` | [`FileCommentObject`](../../doc/models/file-comment-object.md) | Optional | - |
| `display_as_bot` | `TrueClass \| FalseClass` | Optional | - |
| `file` | [`FileObject`](../../doc/models/file-object.md) | Optional | - |
| `files` | [`Array[FileObject]`](../../doc/models/file-object.md) | Optional | **Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `icons` | [`Icons1`](../../doc/models/icons-1.md) | Optional | - |
| `inviter` | `String` | Optional | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `is_delayed_message` | `TrueClass \| FalseClass` | Optional | - |
| `is_intro` | `TrueClass \| FalseClass` | Optional | - |
| `is_starred` | `TrueClass \| FalseClass` | Optional | - |
| `last_read` | `String` | Optional | **Constraints**: *Pattern*: `^\d{10}\.\d{6}$` |
| `latest_reply` | `String` | Optional | **Constraints**: *Pattern*: `^\d{10}\.\d{6}$` |
| `name` | `String` | Optional | - |
| `old_name` | `String` | Optional | - |
| `parent_user_id` | `String` | Optional | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `permalink` | `String` | Optional | - |
| `pinned_to` | `Array[String]` | Optional | **Constraints**: *Pattern*: `^[CGD][A-Z0-9]{8,}$` |
| `purpose` | `String` | Optional | - |
| `reactions` | [`Array[ReactionObject]`](../../doc/models/reaction-object.md) | Optional | - |
| `reply_count` | `Integer` | Optional | - |
| `reply_users` | `Array[String]` | Optional | **Constraints**: *Minimum Items*: `1`, *Unique Items Required*, *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `reply_users_count` | `Integer` | Optional | - |
| `source_team` | `String` | Optional | **Constraints**: *Pattern*: `^[TE][A-Z0-9]{8,}$` |
| `subscribed` | `TrueClass \| FalseClass` | Optional | - |
| `subtype` | `String` | Optional | - |
| `team` | `String` | Optional | **Constraints**: *Pattern*: `^[TE][A-Z0-9]{8,}$` |
| `text` | `String` | Required | - |
| `thread_ts` | `String` | Optional | **Constraints**: *Pattern*: `^\d{10}\.\d{6}$` |
| `topic` | `String` | Optional | - |
| `ts` | `String` | Required | **Constraints**: *Pattern*: `^\d{10}\.\d{6}$` |
| `type` | `String` | Required | - |
| `unread_count` | `Integer` | Optional | - |
| `upload` | `TrueClass \| FalseClass` | Optional | - |
| `user` | `String` | Optional | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `user_profile` | [`ObjsUserProfileShort`](../../doc/models/objs-user-profile-short.md) | Optional | - |
| `user_team` | `String` | Optional | **Constraints**: *Pattern*: `^[TE][A-Z0-9]{8,}$` |
| `username` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
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
  "text": "text8",
  "ts": "ts0",
  "type": "type8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

