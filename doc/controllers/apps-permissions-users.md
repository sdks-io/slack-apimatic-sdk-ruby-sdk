# Apps Permissions Users

```ruby
apps_permissions_users_api = client.apps_permissions_users
```

## Class Name

`AppsPermissionsUsersApi`

## Methods

* [Apps Permissions Users List](../../doc/controllers/apps-permissions-users.md#apps-permissions-users-list)
* [Apps Permissions Users Request](../../doc/controllers/apps-permissions-users.md#apps-permissions-users-request)


# Apps Permissions Users List

Returns list of user grants and corresponding scopes this app has on a team.

API method documentation: [https://api.slack.com/methods/apps.permissions.users.list](https://api.slack.com/methods/apps.permissions.users.list)

```ruby
def apps_permissions_users_list(token,
                                cursor: nil,
                                limit: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `none` |
| `cursor` | `String` | Query, Optional | Paginate through collections of data by setting the `cursor` parameter to a `next_cursor` attribute returned by a previous request's `response_metadata`. Default value fetches the first "page" of the collection. See [pagination](/docs/pagination) for more detail. |
| `limit` | `Integer` | Query, Optional | The maximum number of items to return. |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

result = apps_permissions_users_api.apps_permissions_users_list(token)

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


# Apps Permissions Users Request

Enables an app to trigger a permissions modal to grant an app access to a user access scope.

API method documentation: [https://api.slack.com/methods/apps.permissions.users.request](https://api.slack.com/methods/apps.permissions.users.request)

```ruby
def apps_permissions_users_request(token,
                                   scopes,
                                   trigger_id,
                                   user)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `none` |
| `scopes` | `String` | Query, Required | A comma separated list of user scopes to request for |
| `trigger_id` | `String` | Query, Required | Token used to trigger the request |
| `user` | `String` | Query, Required | The user this scope is being requested for |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

scopes = 'scopes4'

trigger_id = 'trigger_id6'

user = 'user0'

result = apps_permissions_users_api.apps_permissions_users_request(
  token,
  scopes,
  trigger_id,
  user
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
| Default | Standard failure response when trigger_id is invalid | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |

