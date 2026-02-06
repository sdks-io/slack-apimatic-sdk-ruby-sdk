
# Prefs

*This model accepts additional fields of type Object.*

## Structure

`Prefs`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channels` | `Array[String]` | Required | **Constraints**: *Pattern*: `^[C][A-Z0-9]{2,}$` |
| `groups` | `Array[String]` | Required | **Constraints**: *Pattern*: `^[G][A-Z0-9]{8,}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "channels": [
    "channels3",
    "channels4",
    "channels5"
  ],
  "groups": [
    "groups6",
    "groups7"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

