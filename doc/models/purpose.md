
# Purpose

*This model accepts additional fields of type Object.*

## Structure

`Purpose`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `creator` | `String` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{8,}$\|^$` |
| `last_set` | `Integer` | Required | - |
| `value` | `String` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "creator": "creator6",
  "last_set": 108,
  "value": "value0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

