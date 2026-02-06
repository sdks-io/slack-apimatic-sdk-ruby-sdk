# Admin Teams Admins

```ruby
admin_teams_admins_api = client.admin_teams_admins
```

## Class Name

`AdminTeamsAdminsApi`


# Admin Teams Admins List

List all of the admins on a given workspace.

API method documentation: [https://api.slack.com/methods/admin.teams.admins.list](https://api.slack.com/methods/admin.teams.admins.list)

```ruby
def admin_teams_admins_list(token,
                            team_id,
                            limit: nil,
                            cursor: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `admin.teams:read` |
| `team_id` | `String` | Query, Required | - |
| `limit` | `Integer` | Query, Optional | The maximum number of items to return. |
| `cursor` | `String` | Query, Optional | Set `cursor` to `next_cursor` returned by the previous call to list items in the next page. |

## Requires scope

### slackAuth

`admin.teams:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

result = admin_teams_admins_api.admin_teams_admins_list(
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

