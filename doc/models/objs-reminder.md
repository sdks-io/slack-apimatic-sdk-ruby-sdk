
# Objs Reminder

*This model accepts additional fields of type Object.*

## Structure

`ObjsReminder`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `complete_ts` | `Integer` | Optional | - |
| `creator` | `String` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^Rm[A-Z0-9]{8,}$` |
| `recurring` | `TrueClass \| FalseClass` | Required | - |
| `text` | `String` | Required | - |
| `time` | `Integer` | Optional | - |
| `user` | `String` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "complete_ts": 102,
  "creator": "creator4",
  "id": "id6",
  "recurring": false,
  "text": "text4",
  "time": 252,
  "user": "user6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

