
# Objs Team Profile Field

*This model accepts additional fields of type Object.*

## Structure

`ObjsTeamProfileField`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `field_name` | `String` | Optional | - |
| `hint` | `String` | Required | - |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^X[a-zA-Z0-9]{9,}$` |
| `is_hidden` | `TrueClass \| FalseClass` | Optional | - |
| `label` | `String` | Required | - |
| `options` | `Object` | Optional | - |
| `ordering` | `Float` | Required | - |
| `possible_values` | `Array[String]` | Optional | - |
| `type` | [`Type`](../../doc/models/type.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "field_name": "field_name4",
  "hint": "hint0",
  "id": "id0",
  "is_hidden": false,
  "label": "label0",
  "options": {
    "key1": "val1",
    "key2": "val2"
  },
  "ordering": 211.1,
  "possible_values": [
    "possible_values1",
    "possible_values2"
  ],
  "type": "options_list",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

