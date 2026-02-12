
# Admin Conversations Convert to Private Error Schema Exception

Schema for error response from admin.conversations.convertToPrivate

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsConvertToPrivateErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`AdminConversationsConvertToPrivateErrorEnum`](../../doc/models/admin-conversations-convert-to-private-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "default_org_wide_channel",
  "ok": "False",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

