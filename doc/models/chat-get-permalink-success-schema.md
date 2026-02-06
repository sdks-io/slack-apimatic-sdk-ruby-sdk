
# Chat Get Permalink Success Schema

Schema for successful response chat.getPermalink

*This model accepts additional fields of type Object.*

## Structure

`ChatGetPermalinkSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `String` | Required | **Constraints**: *Pattern*: `^[CGD][A-Z0-9]{8,}$` |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `permalink` | `String` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "channel": "channel8",
  "ok": "True",
  "permalink": "permalink4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

