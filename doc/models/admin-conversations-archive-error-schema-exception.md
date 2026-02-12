
# Admin Conversations Archive Error Schema Exception

Schema for error response from admin.conversations.archive

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsArchiveErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`AdminConversationsArchiveErrorEnum`](../../doc/models/admin-conversations-archive-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "already_archived",
  "ok": "False",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

