# Admin Apps Requests

```ruby
admin_apps_requests_api = client.admin_apps_requests
```

## Class Name

`AdminAppsRequestsApi`


# Admin Apps Requests List

List app requests for a team/workspace.

API method documentation: [https://api.slack.com/methods/admin.apps.requests.list](https://api.slack.com/methods/admin.apps.requests.list)

```ruby
def admin_apps_requests_list(token,
                             limit: nil,
                             cursor: nil,
                             team_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `admin.apps:read` |
| `limit` | `Integer` | Query, Optional | The maximum number of items to return. Must be between 1 - 1000 both inclusive. |
| `cursor` | `String` | Query, Optional | Set `cursor` to `next_cursor` returned by the previous call to list items in the next page |
| `team_id` | `String` | Query, Optional | - |

## Requires scope

### slackAuth

`admin.apps:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

result = admin_apps_requests_api.admin_apps_requests_list(token)

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

