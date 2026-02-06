
# Attachment

*This model accepts additional fields of type Object.*

## Structure

`Attachment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `fallback` | `String` | Optional | - |
| `id` | `Integer` | Required | - |
| `image_bytes` | `Integer` | Optional | - |
| `image_height` | `Integer` | Optional | - |
| `image_url` | `String` | Optional | - |
| `image_width` | `Integer` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "fallback": "fallback4",
  "id": 158,
  "image_bytes": 168,
  "image_height": 20,
  "image_url": "image_url6",
  "image_width": 146,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

