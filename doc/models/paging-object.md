
# Paging Object

*This model accepts additional fields of type Object.*

## Structure

`PagingObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `count` | `Integer` | Optional | - |
| `page` | `Integer` | Required | - |
| `pages` | `Integer` | Optional | - |
| `per_page` | `Integer` | Optional | - |
| `spill` | `Integer` | Optional | - |
| `total` | `Integer` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "count": 190,
  "page": 160,
  "pages": 28,
  "per_page": 72,
  "spill": 132,
  "total": 140,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

