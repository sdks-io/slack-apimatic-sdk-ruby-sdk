
# Scopes

*This model accepts additional fields of type Object.*

## Structure

`Scopes`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_home` | `Array[String]` | Optional | - |
| `channel` | `Array[String]` | Optional | - |
| `group` | `Array[String]` | Optional | - |
| `im` | `Array[String]` | Optional | - |
| `mpim` | `Array[String]` | Optional | - |
| `team` | `Array[String]` | Optional | - |
| `user` | `Array[String]` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "app_home": [
    "app_home2",
    "app_home1",
    "app_home0"
  ],
  "channel": [
    "channel0",
    "channel9"
  ],
  "group": [
    "group9"
  ],
  "im": [
    "im1",
    "im0",
    "im9"
  ],
  "mpim": [
    "mpim0"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

