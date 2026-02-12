
# Admin Conversations Unarchive Error Schema 3 Exception

Schema for error response from admin.conversations.unarchive

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsUnarchiveErrorSchema3Exception`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`AdminConversationsUnarchiveErrorEnum`](../../doc/models/admin-conversations-unarchive-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "restricted_action",
  "ok": "False",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

