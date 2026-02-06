
# Login

*This model accepts additional fields of type Object.*

## Structure

`Login`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `count` | `Integer` | Required | - |
| `country` | `String` | Required | - |
| `date_first` | `Integer` | Required | - |
| `date_last` | `Integer` | Required | - |
| `ip` | `String` | Required | - |
| `isp` | `String` | Required | - |
| `region` | `String` | Required | - |
| `user_agent` | `String` | Required | - |
| `user_id` | `String` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `username` | `String` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "count": 110,
  "country": "country6",
  "date_first": 14,
  "date_last": 2,
  "ip": "ip6",
  "isp": "isp2",
  "region": "region8",
  "user_agent": "user_agent4",
  "user_id": "user_id0",
  "username": "username8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

