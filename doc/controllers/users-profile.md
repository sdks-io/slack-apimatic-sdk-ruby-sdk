# Users Profile

```ruby
users_profile_api = client.users_profile
```

## Class Name

`UsersProfileApi`

## Methods

* [Users Profile Get](../../doc/controllers/users-profile.md#users-profile-get)
* [Users Profile Set](../../doc/controllers/users-profile.md#users-profile-set)


# Users Profile Get

Retrieves a user's profile information.

API method documentation: [https://api.slack.com/methods/users.profile.get](https://api.slack.com/methods/users.profile.get)

```ruby
def users_profile_get(token,
                      include_labels: nil,
                      user: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `users.profile:read` |
| `include_labels` | `TrueClass \| FalseClass` | Query, Optional | Include labels for each ID in custom profile fields |
| `user` | `String` | Query, Optional | User to retrieve profile info for |

## Requires scope

### slackAuth

`users.profile:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsersProfileGetSchema`](../../doc/models/users-profile-get-schema.md).

## Example Usage

```ruby
token = 'token6'

result = users_profile_api.users_profile_get(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`UsersProfileGetErrorSchemaException`](../../doc/models/users-profile-get-error-schema-exception.md) |


# Users Profile Set

Set the profile information for a user.

API method documentation: [https://api.slack.com/methods/users.profile.set](https://api.slack.com/methods/users.profile.set)

```ruby
def users_profile_set(token,
                      name: nil,
                      profile: nil,
                      user: nil,
                      value: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `users.profile:write` |
| `name` | `String` | Form, Optional | Name of a single key to set. Usable only if `profile` is not passed. |
| `profile` | `String` | Form, Optional | Collection of key:value pairs presented as a URL-encoded JSON hash. At most 50 fields may be set. Each field name is limited to 255 characters. |
| `user` | `String` | Form, Optional | ID of user to change. This argument may only be specified by team admins on paid teams. |
| `value` | `String` | Form, Optional | Value to set a single key to. Usable only if `profile` is not passed. |

## Requires scope

### slackAuth

`users.profile:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsersProfileSetSchema`](../../doc/models/users-profile-set-schema.md).

## Example Usage

```ruby
token = 'token6'

result = users_profile_api.users_profile_set(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`UsersProfileSetErrorSchemaException`](../../doc/models/users-profile-set-error-schema-exception.md) |

