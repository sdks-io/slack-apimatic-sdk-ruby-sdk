
# Reminders Add Schema

Schema for successful response from reminders.add method

*This model accepts additional fields of type Object.*

## Structure

`RemindersAddSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `reminder` | [`ObjsReminder`](../../doc/models/objs-reminder.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "ok": "True",
  "reminder": {
    "complete_ts": 136,
    "creator": "creator8",
    "id": "id0",
    "recurring": false,
    "text": "text0",
    "time": 38,
    "user": "user0",
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

