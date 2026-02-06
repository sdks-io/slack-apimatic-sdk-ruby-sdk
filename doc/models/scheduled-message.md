
# Scheduled Message

*This model accepts additional fields of type Object.*

## Structure

`ScheduledMessage`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel_id` | `String` | Required | **Constraints**: *Pattern*: `^[C][A-Z0-9]{2,}$` |
| `date_created` | `Integer` | Required | - |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^[Q][A-Z0-9]{8,}$` |
| `post_at` | `Integer` | Required | - |
| `text` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "channel_id": "channel_id4",
  "date_created": 228,
  "id": "id8",
  "post_at": 128,
  "text": "text8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

