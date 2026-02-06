# Admin Apps Approved

```ruby
admin_apps_approved_api = client.admin_apps_approved
```

## Class Name

`AdminAppsApprovedApi`


# Admin Apps Approved List

List approved apps for an org or workspace.

API method documentation: [https://api.slack.com/methods/admin.apps.approved.list](https://api.slack.com/methods/admin.apps.approved.list)

```ruby
def admin_apps_approved_list(token,
                             limit: nil,
                             cursor: nil,
                             team_id: nil,
                             enterprise_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `admin.apps:read` |
| `limit` | `Integer` | Query, Optional | The maximum number of items to return. Must be between 1 - 1000 both inclusive. |
| `cursor` | `String` | Query, Optional | Set `cursor` to `next_cursor` returned by the previous call to list items in the next page |
| `team_id` | `String` | Query, Optional | - |
| `enterprise_id` | `String` | Query, Optional | - |

## Requires scope

### slackAuth

`admin.apps:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

result = admin_apps_approved_api.admin_apps_approved_list(token)

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

