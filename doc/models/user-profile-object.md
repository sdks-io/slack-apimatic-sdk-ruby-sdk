
# User Profile Object

*This model accepts additional fields of type Object.*

## Structure

`UserProfileObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `always_active` | `TrueClass \| FalseClass` | Optional | - |
| `api_app_id` | `String` | Optional | **Constraints**: *Pattern*: `^(A[A-Z0-9]{1,})?$` |
| `avatar_hash` | `String` | Required | - |
| `bot_id` | `String` | Optional | **Constraints**: *Pattern*: `^B[A-Z0-9]{8,}$` |
| `display_name` | `String` | Required | - |
| `display_name_normalized` | `String` | Required | - |
| `email` | `String` | Optional | - |
| `fields` | `Array[Object]` | Required | - |
| `first_name` | `String` | Optional | - |
| `guest_expiration_ts` | `Integer` | Optional | - |
| `guest_invited_by` | `String` | Optional | - |
| `image_1024` | `String` | Optional | - |
| `image_192` | `String` | Optional | - |
| `image_24` | `String` | Optional | - |
| `image_32` | `String` | Optional | - |
| `image_48` | `String` | Optional | - |
| `image_512` | `String` | Optional | - |
| `image_72` | `String` | Optional | - |
| `image_original` | `String` | Optional | - |
| `is_app_user` | `TrueClass \| FalseClass` | Optional | - |
| `is_custom_image` | `TrueClass \| FalseClass` | Optional | - |
| `is_restricted` | `TrueClass \| FalseClass` | Optional | - |
| `is_ultra_restricted` | `TrueClass \| FalseClass` | Optional | - |
| `last_avatar_image_hash` | `String` | Optional | - |
| `last_name` | `String` | Optional | - |
| `memberships_count` | `Integer` | Optional | - |
| `name` | `String` | Optional | - |
| `phone` | `String` | Required | - |
| `pronouns` | `String` | Optional | - |
| `real_name` | `String` | Required | - |
| `real_name_normalized` | `String` | Required | - |
| `skype` | `String` | Required | - |
| `status_default_emoji` | `String` | Optional | - |
| `status_default_text` | `String` | Optional | - |
| `status_default_text_canonical` | `String` | Optional | - |
| `status_emoji` | `String` | Required | - |
| `status_expiration` | `Integer` | Optional | - |
| `status_text` | `String` | Required | - |
| `status_text_canonical` | `String` | Optional | - |
| `team` | `String` | Optional | **Constraints**: *Pattern*: `^[TE][A-Z0-9]{8,}$` |
| `title` | `String` | Required | - |
| `updated` | `Integer` | Optional | - |
| `user_id` | `String` | Optional | - |
| `username` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "always_active": false,
  "api_app_id": "api_app_id8",
  "avatar_hash": "avatar_hash8",
  "bot_id": "bot_id8",
  "display_name": "display_name8",
  "display_name_normalized": "display_name_normalized8",
  "email": "email8",
  "fields": [
    {
      "key1": "val1",
      "key2": "val2"
    }
  ],
  "first_name": "first_name8",
  "phone": "phone2",
  "real_name": "real_name6",
  "real_name_normalized": "real_name_normalized8",
  "skype": "skype8",
  "status_emoji": "status_emoji2",
  "status_text": "status_text0",
  "title": "title4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

