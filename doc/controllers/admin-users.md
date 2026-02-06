# Admin Users

```ruby
admin_users_api = client.admin_users
```

## Class Name

`AdminUsersApi`

## Methods

* [Admin Users Assign](../../doc/controllers/admin-users.md#admin-users-assign)
* [Admin Users Invite](../../doc/controllers/admin-users.md#admin-users-invite)
* [Admin Users List](../../doc/controllers/admin-users.md#admin-users-list)
* [Admin Users Remove](../../doc/controllers/admin-users.md#admin-users-remove)
* [Admin Users Set Admin](../../doc/controllers/admin-users.md#admin-users-set-admin)
* [Admin Users Set Expiration](../../doc/controllers/admin-users.md#admin-users-set-expiration)
* [Admin Users Set Owner](../../doc/controllers/admin-users.md#admin-users-set-owner)
* [Admin Users Set Regular](../../doc/controllers/admin-users.md#admin-users-set-regular)


# Admin Users Assign

Add an Enterprise user to a workspace.

API method documentation: [https://api.slack.com/methods/admin.users.assign](https://api.slack.com/methods/admin.users.assign)

```ruby
def admin_users_assign(token,
                       team_id,
                       user_id,
                       is_restricted: nil,
                       is_ultra_restricted: nil,
                       channel_ids: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.users:write` |
| `team_id` | `String` | Form, Required | The ID (`T1234`) of the workspace. |
| `user_id` | `String` | Form, Required | The ID of the user to add to the workspace. |
| `is_restricted` | `TrueClass \| FalseClass` | Form, Optional | True if user should be added to the workspace as a guest. |
| `is_ultra_restricted` | `TrueClass \| FalseClass` | Form, Optional | True if user should be added to the workspace as a single-channel guest. |
| `channel_ids` | `String` | Form, Optional | Comma separated values of channel IDs to add user in the new workspace. |

## Requires scope

### slackAuth

`admin.users:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

user_id = 'user_id8'

result = admin_users_api.admin_users_assign(
  token,
  team_id,
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


# Admin Users Invite

Invite a user to a workspace.

API method documentation: [https://api.slack.com/methods/admin.users.invite](https://api.slack.com/methods/admin.users.invite)

```ruby
def admin_users_invite(token,
                       team_id,
                       email,
                       channel_ids,
                       custom_message: nil,
                       real_name: nil,
                       resend: nil,
                       is_restricted: nil,
                       is_ultra_restricted: nil,
                       guest_expiration_ts: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.users:write` |
| `team_id` | `String` | Form, Required | The ID (`T1234`) of the workspace. |
| `email` | `String` | Form, Required | The email address of the person to invite. |
| `channel_ids` | `String` | Form, Required | A comma-separated list of `channel_id`s for this user to join. At least one channel is required. |
| `custom_message` | `String` | Form, Optional | An optional message to send to the user in the invite email. |
| `real_name` | `String` | Form, Optional | Full name of the user. |
| `resend` | `TrueClass \| FalseClass` | Form, Optional | Allow this invite to be resent in the future if a user has not signed up yet. (default: false) |
| `is_restricted` | `TrueClass \| FalseClass` | Form, Optional | Is this user a multi-channel guest user? (default: false) |
| `is_ultra_restricted` | `TrueClass \| FalseClass` | Form, Optional | Is this user a single channel guest user? (default: false) |
| `guest_expiration_ts` | `String` | Form, Optional | Timestamp when guest account should be disabled. Only include this timestamp if you are inviting a guest user and you want their account to expire on a certain date. |

## Requires scope

### slackAuth

`admin.users:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

email = 'email6'

channel_ids = 'channel_ids8'

result = admin_users_api.admin_users_invite(
  token,
  team_id,
  email,
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


# Admin Users List

List users on a workspace

API method documentation: [https://api.slack.com/methods/admin.users.list](https://api.slack.com/methods/admin.users.list)

```ruby
def admin_users_list(token,
                     team_id,
                     cursor: nil,
                     limit: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.users:read` |
| `team_id` | `String` | Query, Required | The ID (`T1234`) of the workspace. |
| `cursor` | `String` | Query, Optional | Set `cursor` to `next_cursor` returned by the previous call to list items in the next page. |
| `limit` | `Integer` | Query, Optional | Limit for how many users to be retrieved per page |

## Requires scope

### slackAuth

`admin.users:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

result = admin_users_api.admin_users_list(
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


# Admin Users Remove

Remove a user from a workspace.

API method documentation: [https://api.slack.com/methods/admin.users.remove](https://api.slack.com/methods/admin.users.remove)

```ruby
def admin_users_remove(token,
                       team_id,
                       user_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.users:write` |
| `team_id` | `String` | Form, Required | The ID (`T1234`) of the workspace. |
| `user_id` | `String` | Form, Required | The ID of the user to remove. |

## Requires scope

### slackAuth

`admin.users:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

user_id = 'user_id8'

result = admin_users_api.admin_users_remove(
  token,
  team_id,
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


# Admin Users Set Admin

Set an existing guest, regular user, or owner to be an admin user.

API method documentation: [https://api.slack.com/methods/admin.users.setAdmin](https://api.slack.com/methods/admin.users.setAdmin)

```ruby
def admin_users_set_admin(token,
                          team_id,
                          user_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.users:write` |
| `team_id` | `String` | Form, Required | The ID (`T1234`) of the workspace. |
| `user_id` | `String` | Form, Required | The ID of the user to designate as an admin. |

## Requires scope

### slackAuth

`admin.users:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

user_id = 'user_id8'

result = admin_users_api.admin_users_set_admin(
  token,
  team_id,
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


# Admin Users Set Expiration

Set an expiration for a guest user

API method documentation: [https://api.slack.com/methods/admin.users.setExpiration](https://api.slack.com/methods/admin.users.setExpiration)

```ruby
def admin_users_set_expiration(token,
                               team_id,
                               user_id,
                               expiration_ts)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.users:write` |
| `team_id` | `String` | Form, Required | The ID (`T1234`) of the workspace. |
| `user_id` | `String` | Form, Required | The ID of the user to set an expiration for. |
| `expiration_ts` | `Integer` | Form, Required | Timestamp when guest account should be disabled. |

## Requires scope

### slackAuth

`admin.users:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

user_id = 'user_id8'

expiration_ts = 186

result = admin_users_api.admin_users_set_expiration(
  token,
  team_id,
  user_id,
  expiration_ts
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


# Admin Users Set Owner

Set an existing guest, regular user, or admin user to be a workspace owner.

API method documentation: [https://api.slack.com/methods/admin.users.setOwner](https://api.slack.com/methods/admin.users.setOwner)

```ruby
def admin_users_set_owner(token,
                          team_id,
                          user_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.users:write` |
| `team_id` | `String` | Form, Required | The ID (`T1234`) of the workspace. |
| `user_id` | `String` | Form, Required | Id of the user to promote to owner. |

## Requires scope

### slackAuth

`admin.users:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

user_id = 'user_id8'

result = admin_users_api.admin_users_set_owner(
  token,
  team_id,
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


# Admin Users Set Regular

Set an existing guest user, admin user, or owner to be a regular user.

API method documentation: [https://api.slack.com/methods/admin.users.setRegular](https://api.slack.com/methods/admin.users.setRegular)

```ruby
def admin_users_set_regular(token,
                            team_id,
                            user_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.users:write` |
| `team_id` | `String` | Form, Required | The ID (`T1234`) of the workspace. |
| `user_id` | `String` | Form, Required | The ID of the user to designate as a regular user. |

## Requires scope

### slackAuth

`admin.users:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

team_id = 'team_id6'

user_id = 'user_id8'

result = admin_users_api.admin_users_set_regular(
  token,
  team_id,
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

