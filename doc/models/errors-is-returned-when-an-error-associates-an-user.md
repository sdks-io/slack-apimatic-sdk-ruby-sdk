
# Errors Is Returned When an Error Associates an User

*This model accepts additional fields of type Object.*

## Structure

`ErrorsIsReturnedWhenAnErrorAssociatesAnUser`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | [`ConversationsInviteErrorEnum`](../../doc/models/conversations-invite-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `user` | `String` | Optional | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "cant_invite",
  "ok": "False",
  "user": "user8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

