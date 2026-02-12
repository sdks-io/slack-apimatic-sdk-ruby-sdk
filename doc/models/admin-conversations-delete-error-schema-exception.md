
# Admin Conversations Delete Error Schema Exception

Schema for error response from admin.conversations.delete

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsDeleteErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`AdminConversationsDeleteErrorEnum`](../../doc/models/admin-conversations-delete-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "could_not_delete_channel",
  "ok": "False",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

