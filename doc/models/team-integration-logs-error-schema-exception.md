
# Team Integration Logs Error Schema Exception

Schema for error response from team.integrationLogs method

*This model accepts additional fields of type Object.*

## Structure

`TeamIntegrationLogsErrorSchemaException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `callstack` | `String` | Optional | Note: PHP callstack is only visible in dev/qa |
| `error` | [`AppsPermissionsInfoErrorEnum`](../../doc/models/apps-permissions-info-error-enum.md) | Required | - |
| `ok` | `String` | Required, Constant | **Value**: `'False'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "error": "fatal_error",
  "ok": "False",
  "callstack": "callstack6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

