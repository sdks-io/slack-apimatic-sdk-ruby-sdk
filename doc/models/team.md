
# Team

*This model accepts additional fields of type Object.*

## Structure

`Team`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resources` | [`ResourcesInInfoFromAppsPermissionsInfo`](../../doc/models/resources-in-info-from-apps-permissions-info.md) | Required | - |
| `scopes` | `Array[String]` | Required | - |
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
    "scopes2"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

