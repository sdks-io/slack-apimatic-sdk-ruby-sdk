
# App Home

*This model accepts additional fields of type Object.*

## Structure

`AppHome`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resources` | [`ResourcesInInfoFromAppsPermissionsInfo`](../../doc/models/resources-in-info-from-apps-permissions-info.md) | Optional | - |
| `scopes` | `Array[String]` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "resources": {
    "excluded_ids": [
      {
        "key1": "val1",
        "key2": "val2"
      },
      {
        "key1": "val1",
        "key2": "val2"
      },
      {
        "key1": "val1",
        "key2": "val2"
      }
    ],
    "ids": [
      {
        "key1": "val1",
        "key2": "val2"
      },
      {
        "key1": "val1",
        "key2": "val2"
      },
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
  },
  "scopes": [
    "scopes2",
    "scopes1"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

