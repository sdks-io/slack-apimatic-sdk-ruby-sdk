
# Reaction Object

*This model accepts additional fields of type Object.*

## Structure

`ReactionObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `count` | `Integer` | Required | - |
| `name` | `String` | Required | - |
| `users` | `Array[String]` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "count": 186,
  "name": "name6",
  "users": [
    "users3",
    "users2"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

