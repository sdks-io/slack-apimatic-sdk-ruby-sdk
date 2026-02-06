
# Chat Delete Success Schema

Schema for successful response of chat.delete method

*This model accepts additional fields of type Object.*

## Structure

`ChatDeleteSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `String` | Required | **Constraints**: *Pattern*: `^[CGD][A-Z0-9]{8,}$` |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `ts` | `String` | Required | **Constraints**: *Pattern*: `^\d{10}\.\d{6}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "channel": "channel4",
  "ok": "True",
  "ts": "ts2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

