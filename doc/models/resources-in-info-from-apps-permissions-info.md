
# Resources in Info From Apps Permissions Info

*This model accepts additional fields of type Object.*

## Structure

`ResourcesInInfoFromAppsPermissionsInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `excluded_ids` | `Array[Object]` | Optional | - |
| `ids` | `Array[Object]` | Required | - |
| `wildcard` | `TrueClass \| FalseClass` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "excluded_ids": [
    {
      "key1": "val1",
      "key2": "val2"
    }
  ],
  "ids": [
    {
      "key1": "val1",
      "key2": "val2"
    }
  ],
  "wildcard": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

