
# Conversations Close Success Schema

Schema for successful response conversations.close method

*This model accepts additional fields of type Object.*

## Structure

`ConversationsCloseSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `already_closed` | `TrueClass \| FalseClass` | Optional | - |
| `no_op` | `TrueClass \| FalseClass` | Optional | - |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "ok": "True",
  "already_closed": false,
  "no_op": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

