
# Admin Conversations Get Teams Error Schema Exception

Schema for error response from admin.conversations.getTeams

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsGetTeamsErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`Error6`](../../doc/models/error-6.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "channel_type_not_supported",
  "ok": "False",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

