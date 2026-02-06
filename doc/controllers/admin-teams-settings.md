# Admin Teams Settings

```ruby
admin_teams_settings_api = client.admin_teams_settings
```

## Class Name

`AdminTeamsSettingsApi`

## Methods

* [Admin Teams Settings Info](../../doc/controllers/admin-teams-settings.md#admin-teams-settings-info)
* [Admin Teams Settings Set Default Channels](../../doc/controllers/admin-teams-settings.md#admin-teams-settings-set-default-channels)
* [Admin Teams Settings Set Description](../../doc/controllers/admin-teams-settings.md#admin-teams-settings-set-description)
* [Admin Teams Settings Set Discoverability](../../doc/controllers/admin-teams-settings.md#admin-teams-settings-set-discoverability)
* [Admin Teams Settings Set Icon](../../doc/controllers/admin-teams-settings.md#admin-teams-settings-set-icon)
* [Admin Teams Settings Set Name](../../doc/controllers/admin-teams-settings.md#admin-teams-settings-set-name)


# Admin Teams Settings Info

Fetch information about settings in a workspace

API method documentation: [https://api.slack.com/methods/admin.teams.settings.info](https://api.slack.com/methods/admin.teams.settings.info)

```ruby
def admin_teams_settings_info(token,
                              team_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.teams:read` |
| `team_id` | `String` | Query, Required | - |

## Requires scope

### slackAuth

`admin.teams:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

result = admin_teams_settings_api.admin_teams_settings_info(
  token,
  team_id
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


# Admin Teams Settings Set Default Channels

Set the default channels of a workspace.

API method documentation: [https://api.slack.com/methods/admin.teams.settings.setDefaultChannels](https://api.slack.com/methods/admin.teams.settings.setDefaultChannels)

```ruby
def admin_teams_settings_set_default_channels(token,
                                              team_id,
                                              channel_ids)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Required | Authentication token. Requires scope: `admin.teams:write` |
| `team_id` | `String` | Form, Required | ID for the workspace to set the default channel for. |
| `channel_ids` | `String` | Form, Required | An array of channel IDs. |

## Requires scope

### slackAuth

`admin.teams:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

channel_ids = 'channel_ids8'

result = admin_teams_settings_api.admin_teams_settings_set_default_channels(
  token,
  team_id,
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
| Default | Typical error response | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |


# Admin Teams Settings Set Description

Set the description of a given workspace.

API method documentation: [https://api.slack.com/methods/admin.teams.settings.setDescription](https://api.slack.com/methods/admin.teams.settings.setDescription)

```ruby
def admin_teams_settings_set_description(token,
                                         team_id,
                                         description)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.teams:write` |
| `team_id` | `String` | Form, Required | ID for the workspace to set the description for. |
| `description` | `String` | Form, Required | The new description for the workspace. |

## Requires scope

### slackAuth

`admin.teams:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

description = 'description0'

result = admin_teams_settings_api.admin_teams_settings_set_description(
  token,
  team_id,
  description
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


# Admin Teams Settings Set Discoverability

An API method that allows admins to set the discoverability of a given workspace

API method documentation: [https://api.slack.com/methods/admin.teams.settings.setDiscoverability](https://api.slack.com/methods/admin.teams.settings.setDiscoverability)

```ruby
def admin_teams_settings_set_discoverability(token,
                                             team_id,
                                             discoverability)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.teams:write` |
| `team_id` | `String` | Form, Required | The ID of the workspace to set discoverability on. |
| `discoverability` | `String` | Form, Required | This workspace's discovery setting. It must be set to one of `open`, `invite_only`, `closed`, or `unlisted`. |

## Requires scope

### slackAuth

`admin.teams:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

discoverability = 'discoverability0'

result = admin_teams_settings_api.admin_teams_settings_set_discoverability(
  token,
  team_id,
  discoverability
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


# Admin Teams Settings Set Icon

Sets the icon of a workspace.

API method documentation: [https://api.slack.com/methods/admin.teams.settings.setIcon](https://api.slack.com/methods/admin.teams.settings.setIcon)

```ruby
def admin_teams_settings_set_icon(token,
                                  image_url,
                                  team_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Required | Authentication token. Requires scope: `admin.teams:write` |
| `image_url` | `String` | Form, Required | Image URL for the icon |
| `team_id` | `String` | Form, Required | ID for the workspace to set the icon for. |

## Requires scope

### slackAuth

`admin.teams:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

image_url = 'image_url6'

team_id = 'team_id6'

result = admin_teams_settings_api.admin_teams_settings_set_icon(
  token,
  image_url,
  team_id
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


# Admin Teams Settings Set Name

Set the name of a given workspace.

API method documentation: [https://api.slack.com/methods/admin.teams.settings.setName](https://api.slack.com/methods/admin.teams.settings.setName)

```ruby
def admin_teams_settings_set_name(token,
                                  team_id,
                                  name)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.teams:write` |
| `team_id` | `String` | Form, Required | ID for the workspace to set the name for. |
| `name` | `String` | Form, Required | The new name of the workspace. |

## Requires scope

### slackAuth

`admin.teams:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

name = 'name0'

result = admin_teams_settings_api.admin_teams_settings_set_name(
  token,
  team_id,
  name
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

