
# Dnd End Snooze Schema

Schema for successful response from dnd.endSnooze method

*This model accepts additional fields of type Object.*

## Structure

`DndEndSnoozeSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dnd_enabled` | `TrueClass \| FalseClass` | Required | - |
| `next_dnd_end_ts` | `Integer` | Required | - |
| `next_dnd_start_ts` | `Integer` | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `snooze_enabled` | `TrueClass \| FalseClass` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "dnd_enabled": false,
  "next_dnd_end_ts": 248,
  "next_dnd_start_ts": 88,
  "ok": "True",
  "snooze_enabled": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

