# Admin Usergroups

```ruby
admin_usergroups_api = client.admin_usergroups
```

## Class Name

`AdminUsergroupsApi`

## Methods

* [Admin Usergroups Add Channels](../../doc/controllers/admin-usergroups.md#admin-usergroups-add-channels)
* [Admin Usergroups Add Teams](../../doc/controllers/admin-usergroups.md#admin-usergroups-add-teams)
* [Admin Usergroups List Channels](../../doc/controllers/admin-usergroups.md#admin-usergroups-list-channels)
* [Admin Usergroups Remove Channels](../../doc/controllers/admin-usergroups.md#admin-usergroups-remove-channels)


# Admin Usergroups Add Channels

Add one or more default channels to an IDP group.

API method documentation: [https://api.slack.com/methods/admin.usergroups.addChannels](https://api.slack.com/methods/admin.usergroups.addChannels)

```ruby
def admin_usergroups_add_channels(token,
                                  usergroup_id,
                                  channel_ids,
                                  team_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.usergroups:write` |
| `usergroup_id` | `String` | Form, Required | ID of the IDP group to add default channels for. |
| `channel_ids` | `String` | Form, Required | Comma separated string of channel IDs. |
| `team_id` | `String` | Form, Optional | The workspace to add default channels in. |

## Requires scope

### slackAuth

`admin.usergroups:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

usergroup_id = 'usergroup_id0'

channel_ids = 'channel_ids8'

result = admin_usergroups_api.admin_usergroups_add_channels(
  token,
  usergroup_id,
  channel_ids
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
| Default | Typical error response if the token provided is not associated with an Org Admin or Owner | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |


# Admin Usergroups Add Teams

Associate one or more default workspaces with an organization-wide IDP group.

API method documentation: [https://api.slack.com/methods/admin.usergroups.addTeams](https://api.slack.com/methods/admin.usergroups.addTeams)

```ruby
def admin_usergroups_add_teams(token,
                               usergroup_id,
                               team_ids,
                               auto_provision: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.teams:write` |
| `usergroup_id` | `String` | Form, Required | An encoded usergroup (IDP Group) ID. |
| `team_ids` | `String` | Form, Required | A comma separated list of encoded team (workspace) IDs. Each workspace *MUST* belong to the organization associated with the token. |
| `auto_provision` | `TrueClass \| FalseClass` | Form, Optional | When `true`, this method automatically creates new workspace accounts for the IDP group members. |

## Requires scope

### slackAuth

`admin.teams:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

usergroup_id = 'usergroup_id0'

team_ids = 'team_ids2'

result = admin_usergroups_api.admin_usergroups_add_teams(
  token,
  usergroup_id,
  team_ids
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


# Admin Usergroups List Channels

List the channels linked to an org-level IDP group (user group).

API method documentation: [https://api.slack.com/methods/admin.usergroups.listChannels](https://api.slack.com/methods/admin.usergroups.listChannels)

```ruby
def admin_usergroups_list_channels(token,
                                   usergroup_id,
                                   team_id: nil,
                                   include_num_members: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.usergroups:read` |
| `usergroup_id` | `String` | Query, Required | ID of the IDP group to list default channels for. |
| `team_id` | `String` | Query, Optional | ID of the the workspace. |
| `include_num_members` | `TrueClass \| FalseClass` | Query, Optional | Flag to include or exclude the count of members per channel. |

## Requires scope

### slackAuth

`admin.usergroups:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

usergroup_id = 'usergroup_id0'

result = admin_usergroups_api.admin_usergroups_list_channels(
  token,
  usergroup_id
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
| Default | Typical error response if the token provided is not associated with an Org Admin or Owner | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |


# Admin Usergroups Remove Channels

Remove one or more default channels from an org-level IDP group (user group).

API method documentation: [https://api.slack.com/methods/admin.usergroups.removeChannels](https://api.slack.com/methods/admin.usergroups.removeChannels)

```ruby
def admin_usergroups_remove_channels(token,
                                     usergroup_id,
                                     channel_ids)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.usergroups:write` |
| `usergroup_id` | `String` | Form, Required | ID of the IDP Group |
| `channel_ids` | `String` | Form, Required | Comma-separated string of channel IDs |

## Requires scope

### slackAuth

`admin.usergroups:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

usergroup_id = 'usergroup_id0'

channel_ids = 'channel_ids8'

result = admin_usergroups_api.admin_usergroups_remove_channels(
  token,
  usergroup_id,
  channel_ids
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
| Default | Typical error response if the token provided is not associated with an Org Admin or Owner | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |

