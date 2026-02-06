
# Team Object

*This model accepts additional fields of type Object.*

## Structure

`TeamObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `archived` | `TrueClass \| FalseClass` | Optional | - |
| `avatar_base_url` | `String` | Optional | - |
| `created` | `Integer` | Optional | - |
| `date_create` | `Integer` | Optional | - |
| `deleted` | `TrueClass \| FalseClass` | Optional | - |
| `description` | `String` | Optional | - |
| `discoverable` | `Object` | Optional | - |
| `domain` | `String` | Required | - |
| `email_domain` | `String` | Required | - |
| `enterprise_id` | `String` | Optional | **Constraints**: *Pattern*: `^[E][A-Z0-9]{8,}$` |
| `enterprise_name` | `String` | Optional | - |
| `external_org_migrations` | [`ExternalOrgMigrations`](../../doc/models/external-org-migrations.md) | Optional | - |
| `has_compliance_export` | `TrueClass \| FalseClass` | Optional | - |
| `icon` | [`ObjsIcon`](../../doc/models/objs-icon.md) | Required | - |
| `id` | `String` | Required | **Constraints**: *Pattern*: `^[TE][A-Z0-9]{8,}$` |
| `is_assigned` | `TrueClass \| FalseClass` | Optional | - |
| `is_enterprise` | `Integer` | Optional | - |
| `is_over_storage_limit` | `TrueClass \| FalseClass` | Optional | - |
| `limit_ts` | `Integer` | Optional | - |
| `locale` | `String` | Optional | - |
| `messages_count` | `Integer` | Optional | - |
| `msg_edit_window_mins` | `Integer` | Optional | - |
| `name` | `String` | Required | - |
| `over_integrations_limit` | `TrueClass \| FalseClass` | Optional | - |
| `over_storage_limit` | `TrueClass \| FalseClass` | Optional | - |
| `pay_prod_cur` | `String` | Optional | - |
| `plan` | [`Plan`](../../doc/models/plan.md) | Optional | - |
| `primary_owner` | [`ObjsPrimaryOwner`](../../doc/models/objs-primary-owner.md) | Optional | - |
| `sso_provider` | [`SsoProvider`](../../doc/models/sso-provider.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "archived": false,
  "avatar_base_url": "avatar_base_url4",
  "created": 18,
  "date_create": 124,
  "deleted": false,
  "domain": "domain0",
  "email_domain": "email_domain4",
  "icon": {
    "image_102": "image_1020",
    "image_132": "image_1326",
    "image_230": "image_2308",
    "image_34": "image_340",
    "image_44": "image_440",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "id": "id4",
  "name": "name4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

