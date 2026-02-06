# Admin Teams

```ruby
admin_teams_api = client.admin_teams
```

## Class Name

`AdminTeamsApi`

## Methods

* [Admin Teams Create](../../doc/controllers/admin-teams.md#admin-teams-create)
* [Admin Teams List](../../doc/controllers/admin-teams.md#admin-teams-list)


# Admin Teams Create

Create an Enterprise team.

API method documentation: [https://api.slack.com/methods/admin.teams.create](https://api.slack.com/methods/admin.teams.create)

```ruby
def admin_teams_create(token,
                       team_domain,
                       team_name,
                       team_description: nil,
                       team_discoverability: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.teams:write` |
| `team_domain` | `String` | Form, Required | Team domain (for example, slacksoftballteam). |
| `team_name` | `String` | Form, Required | Team name (for example, Slack Softball Team). |
| `team_description` | `String` | Form, Optional | Description for the team. |
| `team_discoverability` | `String` | Form, Optional | Who can join the team. A team's discoverability can be `open`, `closed`, `invite_only`, or `unlisted`. |

## Requires scope

### slackAuth

`admin.teams:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_domain = 'team_domain2'

team_name = 'team_name6'

result = admin_teams_api.admin_teams_create(
  token,
  team_domain,
  team_name
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


# Admin Teams List

List all teams on an Enterprise organization

API method documentation: [https://api.slack.com/methods/admin.teams.list](https://api.slack.com/methods/admin.teams.list)

```ruby
def admin_teams_list(token,
                     limit: nil,
                     cursor: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.teams:read` |
| `limit` | `Integer` | Query, Optional | The maximum number of items to return. Must be between 1 - 100 both inclusive. |
| `cursor` | `String` | Query, Optional | Set `cursor` to `next_cursor` returned by the previous call to list items in the next page. |

## Requires scope

### slackAuth

`admin.teams:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

result = admin_teams_api.admin_teams_list(token)

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

