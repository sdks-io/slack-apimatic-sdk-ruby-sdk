
# Prefs 1

*This model accepts additional fields of type Object.*

## Structure

`Prefs1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `can_thread` | [`CanThread`](../../doc/models/can-thread.md) | Optional | - |
| `who_can_post` | [`WhoCanPost`](../../doc/models/who-can-post.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "can_thread": {
    "type": [
      "type1",
      "type0"
    ],
    "user": [
      "user6",
      "user7"
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "who_can_post": {
    "type": [
      "type5",
      "type4"
    ],
    "user": [
      "user0",
      "user1"
    ],
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

