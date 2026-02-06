
# Subteam Usergroup Object

*This model accepts additional fields of type Object.*

## Structure

`SubteamUsergroupObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto_provision` | `TrueClass \| FalseClass` | Required | - |
| `auto_type` | `Object` | Required | - |
| `channel_count` | `Integer` | Optional | - |
| `created_by` | `String` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `date_create` | `Integer` | Required | - |
| `date_delete` | `Integer` | Required | - |
| `date_update` | `Integer` | Required | - |
| `deleted_by` | `Object` | Required | - |
| `description` | `String` | Required | - |
| `enterprise_subteam_id` | `String` | Required | - |
| `handle` | `String` | Required | - |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^S[A-Z0-9]{2,}$` |
| `is_external` | `TrueClass \| FalseClass` | Required | - |
| `is_subteam` | `TrueClass \| FalseClass` | Required | - |
| `is_usergroup` | `TrueClass \| FalseClass` | Required | - |
| `name` | `String` | Required | - |
| `prefs` | [`Prefs`](../../doc/models/prefs.md) | Required | - |
| `team_id` | `String` | Required | **Constraints**: *Pattern*: `^[T][A-Z0-9]{2,}$` |
| `updated_by` | `String` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `user_count` | `Integer` | Optional | - |
| `users` | `Array[String]` | Optional | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "auto_provision": false,
  "auto_type": {
    "key1": "val1",
    "key2": "val2"
  },
  "channel_count": 140,
  "created_by": "created_by4",
  "date_create": 240,
  "date_delete": 32,
  "date_update": 18,
  "deleted_by": {
    "key1": "val1",
    "key2": "val2"
  },
  "description": "description2",
  "enterprise_subteam_id": "enterprise_subteam_id6",
  "handle": "handle4",
  "id": "id8",
  "is_external": false,
  "is_subteam": false,
  "is_usergroup": false,
  "name": "name8",
  "prefs": {
    "channels": [
      "channels5",
      "channels4"
    ],
    "groups": [
      "groups4",
      "groups5",
      "groups6"
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "team_id": "team_id8",
  "updated_by": "updated_by2",
  "user_count": 110,
  "users": [
    "users5",
    "users4"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

