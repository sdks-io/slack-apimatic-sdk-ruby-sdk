# Usergroups Users

```ruby
usergroups_users_api = client.usergroups_users
```

## Class Name

`UsergroupsUsersApi`

## Methods

* [Usergroups Users List](../../doc/controllers/usergroups-users.md#usergroups-users-list)
* [Usergroups Users Update](../../doc/controllers/usergroups-users.md#usergroups-users-update)


# Usergroups Users List

List all users in a User Group

API method documentation: [https://api.slack.com/methods/usergroups.users.list](https://api.slack.com/methods/usergroups.users.list)

```ruby
def usergroups_users_list(token,
                          usergroup,
                          include_disabled: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `usergroups:read` |
| `usergroup` | `String` | Query, Required | The encoded ID of the User Group to update. |
| `include_disabled` | `TrueClass \| FalseClass` | Query, Optional | Allow results that involve disabled User Groups. |

## Requires scope

### slackAuth

`usergroups:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsergroupsUsersListSchema`](../../doc/models/usergroups-users-list-schema.md).

## Example Usage

```ruby
token = 'token6'

usergroup = 'usergroup2'

result = usergroups_users_api.usergroups_users_list(
  token,
  usergroup
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
| Default | Standard failure response when used with an invalid token | [`UsergroupsUsersListErrorSchemaException`](../../doc/models/usergroups-users-list-error-schema-exception.md) |


# Usergroups Users Update

Update the list of users for a User Group

API method documentation: [https://api.slack.com/methods/usergroups.users.update](https://api.slack.com/methods/usergroups.users.update)

```ruby
def usergroups_users_update(token,
                            usergroup,
                            users,
                            include_count: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `usergroups:write` |
| `usergroup` | `String` | Form, Required | The encoded ID of the User Group to update. |
| `users` | `String` | Form, Required | A comma separated string of encoded user IDs that represent the entire list of users for the User Group. |
| `include_count` | `TrueClass \| FalseClass` | Form, Optional | Include the number of users in the User Group. |

## Requires scope

### slackAuth

`usergroups:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsergroupsUsersUpdateSchema`](../../doc/models/usergroups-users-update-schema.md).

## Example Usage

```ruby
token = 'token6'

usergroup = 'usergroup2'

users = 'users6'

result = usergroups_users_api.usergroups_users_update(
  token,
  usergroup,
  users
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
| Default | Typical error response | [`UsergroupsUsersUpdateErrorSchemaException`](../../doc/models/usergroups-users-update-error-schema-exception.md) |

