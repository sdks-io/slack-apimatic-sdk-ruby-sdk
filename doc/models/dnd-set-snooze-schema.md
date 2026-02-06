
# Dnd Set Snooze Schema

Schema for successful response from dnd.setSnooze method

*This model accepts additional fields of type Object.*

## Structure

`DndSetSnoozeSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `snooze_enabled` | `TrueClass \| FalseClass` | Required | - |
| `snooze_endtime` | `Integer` | Required | - |
| `snooze_remaining` | `Integer` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "ok": "True",
  "snooze_enabled": false,
  "snooze_endtime": 8,
  "snooze_remaining": 8,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

