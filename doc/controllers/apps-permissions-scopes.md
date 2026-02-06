# Apps Permissions Scopes

```ruby
apps_permissions_scopes_api = client.apps_permissions_scopes
```

## Class Name

`AppsPermissionsScopesApi`


# Apps Permissions Scopes List

Returns list of scopes this app has on a team.

API method documentation: [https://api.slack.com/methods/apps.permissions.scopes.list](https://api.slack.com/methods/apps.permissions.scopes.list)

```ruby
def apps_permissions_scopes_list(token)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `none` |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ApiPermissionsScopesListSuccessSchema`](../../doc/models/api-permissions-scopes-list-success-schema.md).

## Example Usage

```ruby
token = 'token6'

result = apps_permissions_scopes_api.apps_permissions_scopes_list(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`AppsPermissionsScopesListErrorSchemaException`](../../doc/models/apps-permissions-scopes-list-error-schema-exception.md) |

