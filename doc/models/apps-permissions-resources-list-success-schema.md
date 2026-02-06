
# Apps Permissions Resources List Success Schema

Schema for successful response apps.permissions.resources.list method

*This model accepts additional fields of type Object.*

## Structure

`AppsPermissionsResourcesListSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `resources` | [`Array[Resource]`](../../doc/models/resource.md) | Required | - |
| `response_metadata` | [`ResponseMetadata`](../../doc/models/response-metadata.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "ok": "True",
  "resources": [
    {
      "id": "id0",
      "type": "type0",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "response_metadata": {
    "next_cursor": "next_cursor2",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

