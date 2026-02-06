
# External Org Migrations

*This model accepts additional fields of type Object.*

## Structure

`ExternalOrgMigrations`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `current` | [`Array[Current]`](../../doc/models/current.md) | Required | - |
| `date_updated` | `Integer` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "current": [
    {
      "date_started": 84,
      "team_id": "team_id0",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "date_updated": 8,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

