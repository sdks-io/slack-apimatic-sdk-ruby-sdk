
# File Comment Object

*This model accepts additional fields of type Object.*

## Structure

`FileCommentObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `comment` | `String` | Required | - |
| `created` | `Integer` | Required | - |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^Fc[A-Z0-9]{8,}$` |
| `is_intro` | `TrueClass \| FalseClass` | Required | - |
| `is_starred` | `TrueClass \| FalseClass` | Optional | - |
| `num_stars` | `Integer` | Optional | - |
| `pinned_info` | `Object` | Optional | - |
| `pinned_to` | `Array[String]` | Optional | **Constraints**: *Pattern*: `^[CGD][A-Z0-9]{8,}$` |
| `reactions` | [`Array[ReactionObject]`](../../doc/models/reaction-object.md) | Optional | - |
| `timestamp` | `Integer` | Required | - |
| `user` | `String` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "comment": "comment2",
  "created": 212,
  "id": "id4",
  "is_intro": false,
  "is_starred": false,
  "num_stars": 180,
  "pinned_info": {
    "key1": "val1",
    "key2": "val2"
  },
  "pinned_to": [
    "pinned_to8",
    "pinned_to9"
  ],
  "reactions": [
    {
      "count": 208,
      "name": "name8",
      "users": [
        "users5",
        "users6",
        "users7"
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "count": 208,
      "name": "name8",
      "users": [
        "users5",
        "users6",
        "users7"
      ],
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "timestamp": 66,
  "user": "user4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

