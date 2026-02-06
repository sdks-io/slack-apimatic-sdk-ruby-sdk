
# Admin Conversations Create Schema

Schema for successful response of admin.conversations.create

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsCreateSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel_id` | `String` | Optional | **Constraints**: *Pattern*: `^[C][A-Z0-9]{2,}$` |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "ok": "True",
  "channel_id": "channel_id6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

