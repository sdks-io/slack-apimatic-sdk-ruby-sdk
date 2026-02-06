
# Chat Post Ephemeral Success Schema

Schema for successful response from chat.postEphemeral method

*This model accepts additional fields of type Object.*

## Structure

`ChatPostEphemeralSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message_ts` | `String` | Required | **Constraints**: *Pattern*: `^\d{10}\.\d{6}$` |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "message_ts": "message_ts0",
  "ok": "True",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

