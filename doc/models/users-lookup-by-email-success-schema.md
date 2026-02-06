
# Users Lookup by Email Success Schema

Schema for successful response from users.lookupByEmail method

*This model accepts additional fields of type Object.*

## Structure

`UsersLookupByEmailSuccessSchema`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ok` | `String` | Required, Constant | **Value**: `'True'` |
| `user` | `Object` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "ok": "True",
  "user": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

