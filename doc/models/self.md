
# Self

*This model accepts additional fields of type Object.*

## Structure

`Self`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `name` | `String` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "id6",
  "name": "name6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

