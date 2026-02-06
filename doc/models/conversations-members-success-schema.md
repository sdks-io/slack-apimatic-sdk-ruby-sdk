
# Conversations Members Success Schema

Schema for successful response conversations.members method

*This model accepts additional fields of type Object.*

## Structure

`ConversationsMembersSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `members` | `Array[String]` | Required | **Constraints**: *Minimum Items*: `1`, *Unique Items Required*, *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `response_metadata` | [`ResponseMetadata`](../../doc/models/response-metadata.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "members": [
    "members8",
    "members9"
  ],
  "ok": "True",
  "response_metadata": {
    "next_cursor": "next_cursor2",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

