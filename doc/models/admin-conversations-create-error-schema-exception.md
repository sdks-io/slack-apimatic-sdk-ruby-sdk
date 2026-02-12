
# Admin Conversations Create Error Schema Exception

Schema for error response from admin.conversations.create

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsCreateErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`AdminConversationsCreateErrorEnum`](../../doc/models/admin-conversations-create-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "could_not_create_channel",
  "ok": "False",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

