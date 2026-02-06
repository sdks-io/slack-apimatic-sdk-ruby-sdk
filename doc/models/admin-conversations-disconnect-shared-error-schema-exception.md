
# Admin Conversations Disconnect Shared Error Schema Exception

Schema for error response from admin.conversations.disconnectShared

*This model accepts additional fields of type Object.*

## Structure

`AdminConversationsDisconnectSharedErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`Error4`](../../doc/models/error-4.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "leaving_team_not_in_channel",
  "ok": "False",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

