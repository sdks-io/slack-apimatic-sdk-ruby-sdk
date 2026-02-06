
# Dnd Info Schema

Schema for successful response from dnd.info method

*This model accepts additional fields of type Object.*

## Structure

`DndInfoSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dnd_enabled` | `TrueClass \| FalseClass` | Required | - |
| `next_dnd_end_ts` | `Integer` | Required | - |
| `next_dnd_start_ts` | `Integer` | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `snooze_enabled` | `TrueClass \| FalseClass` | Optional | - |
| `snooze_endtime` | `Integer` | Optional | - |
| `snooze_remaining` | `Integer` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "dnd_enabled": false,
  "next_dnd_end_ts": 138,
  "next_dnd_start_ts": 198,
  "ok": "True",
  "snooze_enabled": false,
  "snooze_endtime": 96,
  "snooze_remaining": 96,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

