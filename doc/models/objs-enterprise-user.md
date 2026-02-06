
# Objs Enterprise User

*This model accepts additional fields of type Object.*

## Structure

`ObjsEnterpriseUser`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enterprise_id` | `String` | Required | **Constraints**: *Pattern*: `^[E][A-Z0-9]{8,}$` |
| `enterprise_name` | `String` | Required | - |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^[WU][A-Z0-9]{8,}$` |
| `is_admin` | `TrueClass \| FalseClass` | Required | - |
| `is_owner` | `TrueClass \| FalseClass` | Required | - |
| `teams` | `Array[String]` | Required | **Constraints**: *Unique Items Required*, *Pattern*: `^[T][A-Z0-9]{2,}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "enterprise_id": "enterprise_id0",
  "enterprise_name": "enterprise_name0",
  "id": "id0",
  "is_admin": false,
  "is_owner": false,
  "teams": [
    "teams3",
    "teams4",
    "teams5"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

