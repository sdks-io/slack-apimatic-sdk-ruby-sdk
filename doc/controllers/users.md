# Users

```ruby
users_api = client.users
```

## Class Name

`UsersApi`

## Methods

* [Users Conversations](../../doc/controllers/users.md#users-conversations)
* [Users Delete Photo](../../doc/controllers/users.md#users-delete-photo)
* [Users Get Presence](../../doc/controllers/users.md#users-get-presence)
* [Users Identity](../../doc/controllers/users.md#users-identity)
* [Users Info](../../doc/controllers/users.md#users-info)
* [Users List](../../doc/controllers/users.md#users-list)
* [Users Lookup by Email](../../doc/controllers/users.md#users-lookup-by-email)
* [Users Set Active](../../doc/controllers/users.md#users-set-active)
* [Users Set Photo](../../doc/controllers/users.md#users-set-photo)
* [Users Set Presence](../../doc/controllers/users.md#users-set-presence)


# Users Conversations

List conversations the calling user may access.

API method documentation: [https://api.slack.com/methods/users.conversations](https://api.slack.com/methods/users.conversations)

```ruby
def users_conversations(token: nil,
                        user: nil,
                        types: nil,
                        exclude_archived: nil,
                        limit: nil,
                        cursor: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `conversations:read` |
| `user` | `String` | Query, Optional | Browse conversations by a specific user ID's membership. Non-public channels are restricted to those where the calling user shares membership. |
| `types` | `String` | Query, Optional | Mix and match channel types by providing a comma-separated list of any combination of `public_channel`, `private_channel`, `mpim`, `im` |
| `exclude_archived` | `TrueClass \| FalseClass` | Query, Optional | Set to `true` to exclude archived channels from the list |
| `limit` | `Integer` | Query, Optional | The maximum number of items to return. Fewer than the requested number of items may be returned, even if the end of the list hasn't been reached. Must be an integer no larger than 1000. |
| `cursor` | `String` | Query, Optional | Paginate through collections of data by setting the `cursor` parameter to a `next_cursor` attribute returned by a previous request's `response_metadata`. Default value fetches the first "page" of the collection. |

## Requires scope

### slackAuth

`channels:read`, `groups:read`, `im:read`, `mpim:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsersConversationsSuccessSchema`](../../doc/models/users-conversations-success-schema.md).

## Example Usage

```ruby
result = users_api.users_conversations

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`UsersConversationsErrorSchemaException`](../../doc/models/users-conversations-error-schema-exception.md) |


# Users Delete Photo

Delete the user profile photo

API method documentation: [https://api.slack.com/methods/users.deletePhoto](https://api.slack.com/methods/users.deletePhoto)

```ruby
def users_delete_photo(token)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Required | Authentication token. Requires scope: `users.profile:write` |

## Requires scope

### slackAuth

`users.profile:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsersDeletePhotoSchema`](../../doc/models/users-delete-photo-schema.md).

## Example Usage

```ruby
token = 'token6'

result = users_api.users_delete_photo(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`UsersDeletePhotoErrorSchemaException`](../../doc/models/users-delete-photo-error-schema-exception.md) |


# Users Get Presence

Gets user presence information.

API method documentation: [https://api.slack.com/methods/users.getPresence](https://api.slack.com/methods/users.getPresence)

```ruby
def users_get_presence(token,
                       user: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `users:read` |
| `user` | `String` | Query, Optional | User to get presence info on. Defaults to the authed user. |

## Requires scope

### slackAuth

`users:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ApiMethodUsersGetPresence`](../../doc/models/api-method-users-get-presence.md).

## Example Usage

```ruby
token = 'token6'

result = users_api.users_get_presence(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`UsersCountsErrorSchemaException`](../../doc/models/users-counts-error-schema-exception.md) |


# Users Identity

Get a user's identity.

API method documentation: [https://api.slack.com/methods/users.identity](https://api.slack.com/methods/users.identity)

```ruby
def users_identity(token: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `identity.basic` |

## Requires scope

### slackAuth

`identity.basic`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type `Mixed`.

## Example Usage

```ruby
result = users_api.users_identity

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response

```
{
  "ok": true,
  "team": {
    "id": "T0G9PQBBK"
  },
  "user": {
    "id": "U0G9QF9C6",
    "name": "Sonny Whether"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`UsersIdentityErrorSchemaException`](../../doc/models/users-identity-error-schema-exception.md) |


# Users Info

Gets information about a user.

API method documentation: [https://api.slack.com/methods/users.info](https://api.slack.com/methods/users.info)

```ruby
def users_info(token,
               include_locale: nil,
               user: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `users:read` |
| `include_locale` | `TrueClass \| FalseClass` | Query, Optional | Set this to `true` to receive the locale for this user. Defaults to `false` |
| `user` | `String` | Query, Optional | User to get info on |

## Requires scope

### slackAuth

`users:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsersInfoSuccessSchema`](../../doc/models/users-info-success-schema.md).

## Example Usage

```ruby
token = 'token6'

result = users_api.users_info(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`UsersInfoErrorSchemaException`](../../doc/models/users-info-error-schema-exception.md) |


# Users List

Lists all users in a Slack team.

API method documentation: [https://api.slack.com/methods/users.list](https://api.slack.com/methods/users.list)

```ruby
def users_list(token: nil,
               limit: nil,
               cursor: nil,
               include_locale: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `users:read` |
| `limit` | `Integer` | Query, Optional | The maximum number of items to return. Fewer than the requested number of items may be returned, even if the end of the users list hasn't been reached. Providing no `limit` value will result in Slack attempting to deliver you the entire result set. If the collection is too large you may experience `limit_required` or HTTP 500 errors. |
| `cursor` | `String` | Query, Optional | Paginate through collections of data by setting the `cursor` parameter to a `next_cursor` attribute returned by a previous request's `response_metadata`. Default value fetches the first "page" of the collection. |
| `include_locale` | `TrueClass \| FalseClass` | Query, Optional | Set this to `true` to receive the locale for users. Defaults to `false` |

## Requires scope

### slackAuth

`users:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsersListSchema`](../../doc/models/users-list-schema.md).

## Example Usage

```ruby
result = users_api.users_list

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`UsersListErrorSchemaException`](../../doc/models/users-list-error-schema-exception.md) |


# Users Lookup by Email

Find a user with an email address.

API method documentation: [https://api.slack.com/methods/users.lookupByEmail](https://api.slack.com/methods/users.lookupByEmail)

```ruby
def users_lookup_by_email(token,
                          email)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `users:read.email` |
| `email` | `String` | Query, Required | An email address belonging to a user in the workspace |

## Requires scope

### slackAuth

`users:read.email`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsersLookupByEmailSuccessSchema`](../../doc/models/users-lookup-by-email-success-schema.md).

## Example Usage

```ruby
token = 'token6'

email = 'email6'

result = users_api.users_lookup_by_email(
  token,
  email
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
| Default | Typical error response | [`UsersLookupByEmailErrorSchemaException`](../../doc/models/users-lookup-by-email-error-schema-exception.md) |


# Users Set Active

Marked a user as active. Deprecated and non-functional.

API method documentation: [https://api.slack.com/methods/users.setActive](https://api.slack.com/methods/users.setActive)

```ruby
def users_set_active(token)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `users:write` |

## Requires scope

### slackAuth

`users:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsersSetActiveSchema`](../../doc/models/users-set-active-schema.md).

## Example Usage

```ruby
token = 'token6'

result = users_api.users_set_active(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`UsersSetActiveErrorSchemaException`](../../doc/models/users-set-active-error-schema-exception.md) |


# Users Set Photo

Set the user profile photo

API method documentation: [https://api.slack.com/methods/users.setPhoto](https://api.slack.com/methods/users.setPhoto)

```ruby
def users_set_photo(token,
                    crop_w: nil,
                    crop_x: nil,
                    crop_y: nil,
                    image: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Required | Authentication token. Requires scope: `users.profile:write` |
| `crop_w` | `String` | Form, Optional | Width/height of crop box (always square) |
| `crop_x` | `String` | Form, Optional | X coordinate of top-left corner of crop box |
| `crop_y` | `String` | Form, Optional | Y coordinate of top-left corner of crop box |
| `image` | `String` | Form, Optional | File contents via `multipart/form-data`. |

## Requires scope

### slackAuth

`users.profile:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsersSetPhotoSchema`](../../doc/models/users-set-photo-schema.md).

## Example Usage

```ruby
token = 'token6'

result = users_api.users_set_photo(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`UsersSetPhotoErrorSchemaException`](../../doc/models/users-set-photo-error-schema-exception.md) |


# Users Set Presence

Manually sets user presence.

API method documentation: [https://api.slack.com/methods/users.setPresence](https://api.slack.com/methods/users.setPresence)

```ruby
def users_set_presence(token,
                       presence)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `users:write` |
| `presence` | `String` | Form, Required | Either `auto` or `away` |

## Requires scope

### slackAuth

`users:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsersSetPresenceSchema`](../../doc/models/users-set-presence-schema.md).

## Example Usage

```ruby
token = 'token6'

presence = 'presence4'

result = users_api.users_set_presence(
  token,
  presence
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
| Default | Typical error response | [`UsersSetPresenceErrorSchemaException`](../../doc/models/users-set-presence-error-schema-exception.md) |

