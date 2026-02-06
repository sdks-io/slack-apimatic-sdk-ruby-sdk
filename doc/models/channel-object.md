
# Channel Object

*This model accepts additional fields of type Object.*

## Structure

`ChannelObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accepted_user` | `String` | Optional | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `created` | `Integer` | Required | - |
| `creator` | `String` | Required | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^[C][A-Z0-9]{2,}$` |
| `is_archived` | `TrueClass \| FalseClass` | Optional | - |
| `is_channel` | `TrueClass \| FalseClass` | Required | - |
| `is_frozen` | `TrueClass \| FalseClass` | Optional | - |
| `is_general` | `TrueClass \| FalseClass` | Optional | - |
| `is_member` | `TrueClass \| FalseClass` | Optional | - |
| `is_moved` | `Integer` | Optional | - |
| `is_mpim` | `TrueClass \| FalseClass` | Required | - |
| `is_non_threadable` | `TrueClass \| FalseClass` | Optional | - |
| `is_org_shared` | `TrueClass \| FalseClass` | Required | - |
| `is_pending_ext_shared` | `TrueClass \| FalseClass` | Optional | - |
| `is_private` | `TrueClass \| FalseClass` | Required | - |
| `is_read_only` | `TrueClass \| FalseClass` | Optional | - |
| `is_shared` | `TrueClass \| FalseClass` | Required | - |
| `is_thread_only` | `TrueClass \| FalseClass` | Optional | - |
| `last_read` | `String` | Optional | **Constraints**: *Pattern*: `^\d{10}\.\d{6}$` |
| `latest` | `Object` | Optional | - |
| `members` | `Array[String]` | Required | **Constraints**: *Minimum Items*: `0`, *Unique Items Required*, *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `name` | `String` | Required | - |
| `name_normalized` | `String` | Required | - |
| `num_members` | `Integer` | Optional | - |
| `pending_shared` | `Array[String]` | Optional | **Constraints**: *Minimum Items*: `0`, *Unique Items Required*, *Pattern*: `^[T][A-Z0-9]{2,}$` |
| `previous_names` | `Array[String]` | Optional | **Constraints**: *Minimum Items*: `0`, *Unique Items Required* |
| `priority` | `Float` | Optional | - |
| `purpose` | [`Purpose`](../../doc/models/purpose.md) | Required | - |
| `topic` | [`Topic`](../../doc/models/topic.md) | Required | - |
| `unlinked` | `Integer` | Optional | - |
| `unread_count` | `Integer` | Optional | - |
| `unread_count_display` | `Integer` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "accepted_user": "accepted_user4",
  "created": 68,
  "creator": "creator4",
  "id": "id6",
  "is_archived": false,
  "is_channel": false,
  "is_frozen": false,
  "is_general": false,
  "is_member": false,
  "is_mpim": false,
  "is_org_shared": false,
  "is_private": false,
  "is_shared": false,
  "members": [
    "members4",
    "members5",
    "members6"
  ],
  "name": "name6",
  "name_normalized": "name_normalized4",
  "purpose": {
    "creator": "creator4",
    "last_set": 30,
    "value": "value8",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "topic": {
    "creator": "creator6",
    "last_set": 242,
    "value": "value0",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

