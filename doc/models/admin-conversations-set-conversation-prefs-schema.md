
# Admin Conversations Set Conversation Prefs Schema

Schema for successful response of admin.conversations.setConversationPrefs

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsSetConversationPrefsSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "ok": "True",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

