
# Users Set Photo Error Schema Exception

Schema for error response from users.setPhoto method

*This model accepts additional fields of type Object.*

## Structure

`UsersSetPhotoErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `callstack` | `String` | Optional | Note: PHP callstack is only visible in dev/qa |
| `debug_step` | `String` | Optional | possibly DEV/QA only |
| `dims` | `String` | Optional | possibly DEV/QA only |
| `error` | [`UsersSetPhotoErrorEnum`](../../doc/models/users-set-photo-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `time_ident` | `Integer` | Optional | possibly DEV/QA only |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "account_inactive",
  "ok": "False",
  "callstack": "callstack4",
  "debug_step": "debug_step0",
  "dims": "dims8",
  "time_ident": 18,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

