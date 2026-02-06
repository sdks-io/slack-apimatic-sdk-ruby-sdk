
# Admin Conversations Unarchive Error Schema 2 Exception

Schema for error response from admin.conversations.rename

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsUnarchiveErrorSchema2Exception`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`Error8`](../../doc/models/error-8.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "name_taken",
  "ok": "False",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

