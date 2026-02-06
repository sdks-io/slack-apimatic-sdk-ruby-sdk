# Admin Conversations Restrict Access

```ruby
admin_conversations_restrict_access_api = client.admin_conversations_restrict_access
```

## Class Name

`AdminConversationsRestrictAccessApi`

## Methods

* [Admin Conversations Restrict Access Add Group](../../doc/controllers/admin-conversations-restrict-access.md#admin-conversations-restrict-access-add-group)
* [Admin Conversations Restrict Access List Groups](../../doc/controllers/admin-conversations-restrict-access.md#admin-conversations-restrict-access-list-groups)
* [Admin Conversations Restrict Access Remove Group](../../doc/controllers/admin-conversations-restrict-access.md#admin-conversations-restrict-access-remove-group)


# Admin Conversations Restrict Access Add Group

Add an allowlist of IDP groups for accessing a channel

API method documentation: [https://api.slack.com/methods/admin.conversations.restrictAccess.addGroup](https://api.slack.com/methods/admin.conversations.restrictAccess.addGroup)

```ruby
def admin_conversations_restrict_access_add_group(token,
                                                  group_id,
                                                  channel_id,
                                                  team_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Required | Authentication token. Requires scope: `admin.conversations:write` |
| `group_id` | `String` | Form, Required | The [IDP Group](https://slack.com/help/articles/115001435788-Connect-identity-provider-groups-to-your-Enterprise-Grid-org) ID to be an allowlist for the private channel. |
| `channel_id` | `String` | Form, Required | The channel to link this group to. |
| `team_id` | `String` | Form, Optional | The workspace where the channel exists. This argument is required for channels only tied to one workspace, and optional for channels that are shared across an organization. |

## Requires scope

### slackAuth

`admin.conversations:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

group_id = 'group_id0'

channel_id = 'channel_id4'

result = admin_conversations_restrict_access_api.admin_conversations_restrict_access_add_group(
  token,
  group_id,
  channel_id
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |


# Admin Conversations Restrict Access List Groups

List all IDP Groups linked to a channel

API method documentation: [https://api.slack.com/methods/admin.conversations.restrictAccess.listGroups](https://api.slack.com/methods/admin.conversations.restrictAccess.listGroups)

```ruby
def admin_conversations_restrict_access_list_groups(token,
                                                    channel_id,
                                                    team_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `admin.conversations:read` |
| `channel_id` | `String` | Query, Required | - |
| `team_id` | `String` | Query, Optional | The workspace where the channel exists. This argument is required for channels only tied to one workspace, and optional for channels that are shared across an organization. |

## Requires scope

### slackAuth

`admin.conversations:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

channel_id = 'channel_id4'

result = admin_conversations_restrict_access_api.admin_conversations_restrict_access_list_groups(
  token,
  channel_id
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |


# Admin Conversations Restrict Access Remove Group

Remove a linked IDP group linked from a private channel

API method documentation: [https://api.slack.com/methods/admin.conversations.restrictAccess.removeGroup](https://api.slack.com/methods/admin.conversations.restrictAccess.removeGroup)

```ruby
def admin_conversations_restrict_access_remove_group(token,
                                                     team_id,
                                                     group_id,
                                                     channel_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Required | Authentication token. Requires scope: `admin.conversations:write` |
| `team_id` | `String` | Form, Required | The workspace where the channel exists. This argument is required for channels only tied to one workspace, and optional for channels that are shared across an organization. |
| `group_id` | `String` | Form, Required | The [IDP Group](https://slack.com/help/articles/115001435788-Connect-identity-provider-groups-to-your-Enterprise-Grid-org) ID to remove from the private channel. |
| `channel_id` | `String` | Form, Required | The channel to remove the linked group from. |

## Requires scope

### slackAuth

`admin.conversations:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

group_id = 'group_id0'

channel_id = 'channel_id4'

result = admin_conversations_restrict_access_api.admin_conversations_restrict_access_remove_group(
  token,
  team_id,
  group_id,
  channel_id
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |

