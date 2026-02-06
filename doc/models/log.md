
# Log

*This model accepts additional fields of type Object.*

## Structure

`Log`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `admin_app_id` | `String` | Optional | **Constraints**: *Pattern*: `^A[A-Z0-9]{1,}$` |
| `app_id` | `String` | Required | **Constraints**: *Pattern*: `^A[A-Z0-9]{1,}$` |
| `app_type` | `String` | Required | - |
| `change_type` | `String` | Required | - |
| `channel` | `String` | Optional | **Constraints**: *Pattern*: `^[CGD][A-Z0-9]{8,}$` |
| `date` | `String` | Required | - |
| `scope` | `String` | Required | - |
| `service_id` | `String` | Optional | - |
| `service_type` | `String` | Optional | - |
| `user_id` | `String` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `user_name` | `String` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "admin_app_id": "admin_app_id2",
  "app_id": "app_id2",
  "app_type": "app_type8",
  "change_type": "change_type2",
  "channel": "channel0",
  "date": "date0",
  "scope": "scope8",
  "service_id": "service_id6",
  "service_type": "service_type0",
  "user_id": "user_id2",
  "user_name": "user_name0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

