
# Admin Conversations Unarchive Error Schema Exception

Schema for error response from admin.conversations.getConversationPrefs

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsUnarchiveErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`AdminConversationsGetConversationPrefsErrorEnum`](../../doc/models/admin-conversations-get-conversation-prefs-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "missing_scope",
  "ok": "False",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

