
# Admin Conversations Invite Error Schema Exception

Schema for error response from admin.conversations.invite

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsInviteErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`AdminConversationsInviteErrorEnum`](../../doc/models/admin-conversations-invite-error-enum.md) | Required | - |
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

