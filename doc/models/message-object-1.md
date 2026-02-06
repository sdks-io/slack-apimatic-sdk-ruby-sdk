
# Message Object 1

*This model accepts additional fields of type Object.*

## Structure

`MessageObject1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `attachments` | `Array[Object]` | Optional | - |
| `blocks` | `Object` | Optional | - |
| `text` | `String` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "attachments": [
    {
      "key1": "val1",
      "key2": "val2"
    },
    {
      "key1": "val1",
      "key2": "val2"
    }
  ],
  "blocks": {
    "key1": "val1",
    "key2": "val2"
  },
  "text": "text4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

