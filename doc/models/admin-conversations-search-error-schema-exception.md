
# Admin Conversations Search Error Schema Exception

Schema for error response from admin.conversations.search

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsSearchErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`AdminConversationsSearchErrorEnum`](../../doc/models/admin-conversations-search-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "invalid_cursor",
  "ok": "False",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

