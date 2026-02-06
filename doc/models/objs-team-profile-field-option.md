
# Objs Team Profile Field Option

*This model accepts additional fields of type Object.*

## Structure

`ObjsTeamProfileFieldOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `is_custom` | `TrueClass \| FalseClass` | Optional | - |
| `is_multiple_entry` | `TrueClass \| FalseClass` | Optional | - |
| `is_protected` | `TrueClass \| FalseClass` | Optional | - |
| `is_scim` | `TrueClass \| FalseClass` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "is_custom": false,
  "is_multiple_entry": false,
  "is_protected": false,
  "is_scim": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

