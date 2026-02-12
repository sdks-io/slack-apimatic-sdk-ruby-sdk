
# Admin Conversations Set Conversation Prefs Error Schema Exception

Schema for error response from admin.conversations.setConversationPrefs

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsSetConversationPrefsErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`AdminConversationsSetConversationPrefsErrorEnum`](../../doc/models/admin-conversations-set-conversation-prefs-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "channel_not_found",
  "ok": "False",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

