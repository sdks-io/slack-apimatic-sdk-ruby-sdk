
# Response Metadata 3

*This model accepts additional fields of type Object.*

## Structure

`ResponseMetadata3`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `warnings` | `Array[String]` | Optional | **Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "warnings": [
    "warnings4",
    "warnings5"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

