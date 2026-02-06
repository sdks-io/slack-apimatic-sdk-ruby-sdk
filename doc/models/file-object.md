
# File Object

*This model accepts additional fields of type Object.*

## Structure

`FileObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channels` | `Array[String]` | Optional | **Constraints**: *Unique Items Required*, *Pattern*: `^[C][A-Z0-9]{2,}$` |
| `comments_count` | `Integer` | Optional | - |
| `created` | `Integer` | Optional | - |
| `date_delete` | `Integer` | Optional | - |
| `display_as_bot` | `TrueClass \| FalseClass` | Optional | - |
| `editable` | `TrueClass \| FalseClass` | Optional | - |
| `editor` | `String` | Optional | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `external_id` | `String` | Optional | - |
| `external_type` | `String` | Optional | - |
| `external_url` | `String` | Optional | - |
| `filetype` | `String` | Optional | - |
| `groups` | `Array[String]` | Optional | **Constraints**: *Unique Items Required*, *Pattern*: `^[G][A-Z0-9]{8,}$` |
| `has_rich_preview` | `TrueClass \| FalseClass` | Optional | - |
| `id` | `String` | Optional | **Constraints**: *Pattern*: `^[F][A-Z0-9]{8,}$` |
| `image_exif_rotation` | `Integer` | Optional | - |
| `ims` | `Array[String]` | Optional | **Constraints**: *Unique Items Required*, *Pattern*: `^[D][A-Z0-9]{8,}$` |
| `is_external` | `TrueClass \| FalseClass` | Optional | - |
| `is_public` | `TrueClass \| FalseClass` | Optional | - |
| `is_starred` | `TrueClass \| FalseClass` | Optional | - |
| `is_tombstoned` | `TrueClass \| FalseClass` | Optional | - |
| `last_editor` | `String` | Optional | **Constraints**: *Pattern*: `^[UW][A-Z0-9]{2,}$` |
| `mimetype` | `String` | Optional | - |
| `mode` | `String` | Optional | - |
| `name` | `String` | Optional | - |
| `non_owner_editable` | `TrueClass \| FalseClass` | Optional | - |
| `num_stars` | `Integer` | Optional | - |
| `original_h` | `Integer` | Optional | - |
| `original_w` | `Integer` | Optional | - |
| `permalink` | `String` | Optional | - |
| `permalink_public` | `String` | Optional | - |
| `pinned_info` | `Object` | Optional | - |
| `pinned_to` | `Array[String]` | Optional | **Constraints**: *Pattern*: `^[CGD][A-Z0-9]{8,}$` |
| `pretty_type` | `String` | Optional | - |
| `preview` | `String` | Optional | - |
| `public_url_shared` | `TrueClass \| FalseClass` | Optional | - |
| `reactions` | [`Array[ReactionObject]`](../../doc/models/reaction-object.md) | Optional | - |
| `shares` | [`Shares`](../../doc/models/shares.md) | Optional | - |
| `size` | `Integer` | Optional | - |
| `source_team` | `String` | Optional | **Constraints**: *Pattern*: `^[T][A-Z0-9]{2,}$` |
| `state` | `String` | Optional | - |
| `thumb_1024` | `String` | Optional | - |
| `thumb_1024_h` | `Integer` | Optional | - |
| `thumb_1024_w` | `Integer` | Optional | - |
| `thumb_160` | `String` | Optional | - |
| `thumb_360` | `String` | Optional | - |
| `thumb_360_h` | `Integer` | Optional | - |
| `thumb_360_w` | `Integer` | Optional | - |
| `thumb_480` | `String` | Optional | - |
| `thumb_480_h` | `Integer` | Optional | - |
| `thumb_480_w` | `Integer` | Optional | - |
| `thumb_64` | `String` | Optional | - |
| `thumb_720` | `String` | Optional | - |
| `thumb_720_h` | `Integer` | Optional | - |
| `thumb_720_w` | `Integer` | Optional | - |
| `thumb_80` | `String` | Optional | - |
| `thumb_800` | `String` | Optional | - |
| `thumb_800_h` | `Integer` | Optional | - |
| `thumb_800_w` | `Integer` | Optional | - |
| `thumb_960` | `String` | Optional | - |
| `thumb_960_h` | `Integer` | Optional | - |
| `thumb_960_w` | `Integer` | Optional | - |
| `thumb_tiny` | `String` | Optional | - |
| `timestamp` | `Integer` | Optional | - |
| `title` | `String` | Optional | - |
| `updated` | `Integer` | Optional | - |
| `url_private` | `String` | Optional | - |
| `url_private_download` | `String` | Optional | - |
| `user` | `String` | Optional | - |
| `user_team` | `String` | Optional | **Constraints**: *Pattern*: `^[T][A-Z0-9]{2,}$` |
| `username` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "channels": [
    "channels3",
    "channels2",
    "channels1"
  ],
  "comments_count": 94,
  "created": 2,
  "date_delete": 156,
  "display_as_bot": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

