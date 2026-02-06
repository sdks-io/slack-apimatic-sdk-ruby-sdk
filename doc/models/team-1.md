
# Team 1

*This model accepts additional fields of type Object.*

## Structure

`Team1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domain` | `String` | Required | - |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^[T][A-Z0-9]{2,}$` |
| `name` | `String` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "domain": "domain0",
  "id": "id4",
  "name": "name4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

