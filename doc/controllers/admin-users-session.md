# Admin Users Session

```ruby
admin_users_session_api = client.admin_users_session
```

## Class Name

`AdminUsersSessionApi`

## Methods

* [Admin Users Session Invalidate](../../doc/controllers/admin-users-session.md#admin-users-session-invalidate)
* [Admin Users Session Reset](../../doc/controllers/admin-users-session.md#admin-users-session-reset)


# Admin Users Session Invalidate

Invalidate a single session for a user by session_id

API method documentation: [https://api.slack.com/methods/admin.users.session.invalidate](https://api.slack.com/methods/admin.users.session.invalidate)

```ruby
def admin_users_session_invalidate(token,
                                   team_id,
                                   session_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.users:write` |
| `team_id` | `String` | Form, Required | ID of the team that the session belongs to |
| `session_id` | `Integer` | Form, Required | - |

## Requires scope

### slackAuth

`admin.users:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

session_id = 2

result = admin_users_session_api.admin_users_session_invalidate(
  token,
  team_id,
  session_id
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


# Admin Users Session Reset

Wipes all valid sessions on all devices for a given user

API method documentation: [https://api.slack.com/methods/admin.users.session.reset](https://api.slack.com/methods/admin.users.session.reset)

```ruby
def admin_users_session_reset(token,
                              user_id,
                              mobile_only: nil,
                              web_only: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.users:write` |
| `user_id` | `String` | Form, Required | The ID of the user to wipe sessions for |
| `mobile_only` | `TrueClass \| FalseClass` | Form, Optional | Only expire mobile sessions (default: false) |
| `web_only` | `TrueClass \| FalseClass` | Form, Optional | Only expire web sessions (default: false) |

## Requires scope

### slackAuth

`admin.users:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

user_id = 'user_id8'

result = admin_users_session_api.admin_users_session_reset(
  token,
  user_id
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

