# Admin Invite Requests

```ruby
admin_invite_requests_api = client.admin_invite_requests
```

## Class Name

`AdminInviteRequestsApi`

## Methods

* [Admin Invite Requests Approve](../../doc/controllers/admin-invite-requests.md#admin-invite-requests-approve)
* [Admin Invite Requests Deny](../../doc/controllers/admin-invite-requests.md#admin-invite-requests-deny)
* [Admin Invite Requests List](../../doc/controllers/admin-invite-requests.md#admin-invite-requests-list)


# Admin Invite Requests Approve

Approve a workspace invite request.

API method documentation: [https://api.slack.com/methods/admin.inviteRequests.approve](https://api.slack.com/methods/admin.inviteRequests.approve)

```ruby
def admin_invite_requests_approve(token,
                                  invite_request_id,
                                  team_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.invites:write` |
| `invite_request_id` | `String` | Form, Required | ID of the request to invite. |
| `team_id` | `String` | Form, Optional | ID for the workspace where the invite request was made. |

## Requires scope

### slackAuth

`admin.invites:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

invite_request_id = 'invite_request_id4'

result = admin_invite_requests_api.admin_invite_requests_approve(
  token,
  invite_request_id
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


# Admin Invite Requests Deny

Deny a workspace invite request.

API method documentation: [https://api.slack.com/methods/admin.inviteRequests.deny](https://api.slack.com/methods/admin.inviteRequests.deny)

```ruby
def admin_invite_requests_deny(token,
                               invite_request_id,
                               team_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.invites:write` |
| `invite_request_id` | `String` | Form, Required | ID of the request to invite. |
| `team_id` | `String` | Form, Optional | ID for the workspace where the invite request was made. |

## Requires scope

### slackAuth

`admin.invites:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

invite_request_id = 'invite_request_id4'

result = admin_invite_requests_api.admin_invite_requests_deny(
  token,
  invite_request_id
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


# Admin Invite Requests List

List all pending workspace invite requests.

API method documentation: [https://api.slack.com/methods/admin.inviteRequests.list](https://api.slack.com/methods/admin.inviteRequests.list)

```ruby
def admin_invite_requests_list(token,
                               team_id: nil,
                               cursor: nil,
                               limit: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.invites:read` |
| `team_id` | `String` | Query, Optional | ID for the workspace where the invite requests were made. |
| `cursor` | `String` | Query, Optional | Value of the `next_cursor` field sent as part of the previous API response |
| `limit` | `Integer` | Query, Optional | The number of results that will be returned by the API on each invocation. Must be between 1 - 1000, both inclusive |

## Requires scope

### slackAuth

`admin.invites:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

result = admin_invite_requests_api.admin_invite_requests_list(token)

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

