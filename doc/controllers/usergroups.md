# Usergroups

```ruby
usergroups_api = client.usergroups
```

## Class Name

`UsergroupsApi`

## Methods

* [Usergroups Create](../../doc/controllers/usergroups.md#usergroups-create)
* [Usergroups Disable](../../doc/controllers/usergroups.md#usergroups-disable)
* [Usergroups Enable](../../doc/controllers/usergroups.md#usergroups-enable)
* [Usergroups List](../../doc/controllers/usergroups.md#usergroups-list)
* [Usergroups Update](../../doc/controllers/usergroups.md#usergroups-update)


# Usergroups Create

Create a User Group

API method documentation: [https://api.slack.com/methods/usergroups.create](https://api.slack.com/methods/usergroups.create)

```ruby
def usergroups_create(token,
                      name,
                      channels: nil,
                      description: nil,
                      handle: nil,
                      include_count: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `usergroups:write` |
| `name` | `String` | Form, Required | A name for the User Group. Must be unique among User Groups. |
| `channels` | `String` | Form, Optional | A comma separated string of encoded channel IDs for which the User Group uses as a default. |
| `description` | `String` | Form, Optional | A short description of the User Group. |
| `handle` | `String` | Form, Optional | A mention handle. Must be unique among channels, users and User Groups. |
| `include_count` | `TrueClass \| FalseClass` | Form, Optional | Include the number of users in each User Group. |

## Requires scope

### slackAuth

`usergroups:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsergroupsCreateSchema`](../../doc/models/usergroups-create-schema.md).

## Example Usage

```ruby
token = 'token6'

name = 'name0'

result = usergroups_api.usergroups_create(
  token,
  name
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
| Default | Typical error response | [`UsergroupsCreateErrorSchemaException`](../../doc/models/usergroups-create-error-schema-exception.md) |


# Usergroups Disable

Disable an existing User Group

API method documentation: [https://api.slack.com/methods/usergroups.disable](https://api.slack.com/methods/usergroups.disable)

```ruby
def usergroups_disable(token,
                       usergroup,
                       include_count: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `usergroups:write` |
| `usergroup` | `String` | Form, Required | The encoded ID of the User Group to disable. |
| `include_count` | `TrueClass \| FalseClass` | Form, Optional | Include the number of users in the User Group. |

## Requires scope

### slackAuth

`usergroups:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsergroupsDisableSchema`](../../doc/models/usergroups-disable-schema.md).

## Example Usage

```ruby
token = 'token6'

usergroup = 'usergroup2'

result = usergroups_api.usergroups_disable(
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
| Default | Typical error response | [`UsergroupsDisableErrorSchemaException`](../../doc/models/usergroups-disable-error-schema-exception.md) |


# Usergroups Enable

Enable a User Group

API method documentation: [https://api.slack.com/methods/usergroups.enable](https://api.slack.com/methods/usergroups.enable)

```ruby
def usergroups_enable(token,
                      usergroup,
                      include_count: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `usergroups:write` |
| `usergroup` | `String` | Form, Required | The encoded ID of the User Group to enable. |
| `include_count` | `TrueClass \| FalseClass` | Form, Optional | Include the number of users in the User Group. |

## Requires scope

### slackAuth

`usergroups:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsergroupsEnableSchema`](../../doc/models/usergroups-enable-schema.md).

## Example Usage

```ruby
token = 'token6'

usergroup = 'usergroup2'

result = usergroups_api.usergroups_enable(
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
| Default | Typical error response | [`UsergroupsEnableErrorSchemaException`](../../doc/models/usergroups-enable-error-schema-exception.md) |


# Usergroups List

List all User Groups for a team

API method documentation: [https://api.slack.com/methods/usergroups.list](https://api.slack.com/methods/usergroups.list)

```ruby
def usergroups_list(token,
                    include_users: nil,
                    include_count: nil,
                    include_disabled: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `usergroups:read` |
| `include_users` | `TrueClass \| FalseClass` | Query, Optional | Include the list of users for each User Group. |
| `include_count` | `TrueClass \| FalseClass` | Query, Optional | Include the number of users in each User Group. |
| `include_disabled` | `TrueClass \| FalseClass` | Query, Optional | Include disabled User Groups. |

## Requires scope

### slackAuth

`usergroups:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsergroupsListSchema`](../../doc/models/usergroups-list-schema.md).

## Example Usage

```ruby
token = 'token6'

result = usergroups_api.usergroups_list(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`UsergroupsListErrorSchemaException`](../../doc/models/usergroups-list-error-schema-exception.md) |


# Usergroups Update

Update an existing User Group

API method documentation: [https://api.slack.com/methods/usergroups.update](https://api.slack.com/methods/usergroups.update)

```ruby
def usergroups_update(token,
                      usergroup,
                      handle: nil,
                      description: nil,
                      channels: nil,
                      include_count: nil,
                      name: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `usergroups:write` |
| `usergroup` | `String` | Form, Required | The encoded ID of the User Group to update. |
| `handle` | `String` | Form, Optional | A mention handle. Must be unique among channels, users and User Groups. |
| `description` | `String` | Form, Optional | A short description of the User Group. |
| `channels` | `String` | Form, Optional | A comma separated string of encoded channel IDs for which the User Group uses as a default. |
| `include_count` | `TrueClass \| FalseClass` | Form, Optional | Include the number of users in the User Group. |
| `name` | `String` | Form, Optional | A name for the User Group. Must be unique among User Groups. |

## Requires scope

### slackAuth

`usergroups:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`UsergroupsUpdateSchema`](../../doc/models/usergroups-update-schema.md).

## Example Usage

```ruby
token = 'token6'

usergroup = 'usergroup2'

result = usergroups_api.usergroups_update(
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
| Default | Typical error response | [`UsergroupsUpdateErrorSchemaException`](../../doc/models/usergroups-update-error-schema-exception.md) |

