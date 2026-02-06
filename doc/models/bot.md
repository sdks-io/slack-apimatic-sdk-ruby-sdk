
# Bot

*This model accepts additional fields of type Object.*

## Structure

`Bot`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_id` | `String` | Required | **Constraints**: *Pattern*: `^A[A-Z0-9]{1,}$` |
| `deleted` | `TrueClass \| FalseClass` | Required | - |
| `icons` | [`Icons`](../../doc/models/icons.md) | Required | - |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^B[A-Z0-9]{8,}$` |
| `name` | `String` | Required | - |
| `updated` | `Integer` | Required | - |
| `user_id` | `String` | Optional | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "app_id": "app_id2",
  "deleted": false,
  "icons": {
    "image_36": "image_362",
    "image_48": "image_488",
    "image_72": "image_722",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "id": "id4",
  "name": "name4",
  "updated": 186,
  "user_id": "user_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

