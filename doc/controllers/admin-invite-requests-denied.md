# Admin Invite Requests Denied

```ruby
admin_invite_requests_denied_api = client.admin_invite_requests_denied
```

## Class Name

`AdminInviteRequestsDeniedApi`


# Admin Invite Requests Denied List

List all denied workspace invite requests.

API method documentation: [https://api.slack.com/methods/admin.inviteRequests.denied.list](https://api.slack.com/methods/admin.inviteRequests.denied.list)

```ruby
def admin_invite_requests_denied_list(token,
                                      team_id: nil,
                                      cursor: nil,
                                      limit: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.invites:read` |
| `team_id` | `String` | Query, Optional | ID for the workspace where the invite requests were made. |
| `cursor` | `String` | Query, Optional | Value of the `next_cursor` field sent as part of the previous api response |
| `limit` | `Integer` | Query, Optional | The number of results that will be returned by the API on each invocation. Must be between 1 - 1000 both inclusive |

## Requires scope

### slackAuth

`admin.invites:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

result = admin_invite_requests_denied_api.admin_invite_requests_denied_list(token)

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

