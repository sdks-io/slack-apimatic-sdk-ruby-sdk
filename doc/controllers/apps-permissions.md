# Apps Permissions

```ruby
apps_permissions_api = client.apps_permissions
```

## Class Name

`AppsPermissionsApi`

## Methods

* [Apps Permissions Info](../../doc/controllers/apps-permissions.md#apps-permissions-info)
* [Apps Permissions Request](../../doc/controllers/apps-permissions.md#apps-permissions-request)


# Apps Permissions Info

Returns list of permissions this app has on a team.

API method documentation: [https://api.slack.com/methods/apps.permissions.info](https://api.slack.com/methods/apps.permissions.info)

```ruby
def apps_permissions_info(token: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `none` |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AppsPermissionsInfoSchema`](../../doc/models/apps-permissions-info-schema.md).

## Example Usage

```ruby
result = apps_permissions_api.apps_permissions_info

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Standard failure response when used with an invalid token | [`AppsPermissionsInfoErrorSchemaException`](../../doc/models/apps-permissions-info-error-schema-exception.md) |


# Apps Permissions Request

Allows an app to request additional scopes

API method documentation: [https://api.slack.com/methods/apps.permissions.request](https://api.slack.com/methods/apps.permissions.request)

```ruby
def apps_permissions_request(token,
                             scopes,
                             trigger_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `none` |
| `scopes` | `String` | Query, Required | A comma separated list of scopes to request for |
| `trigger_id` | `String` | Query, Required | Token used to trigger the permissions API |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AppsPermissionsRequestSchema`](../../doc/models/apps-permissions-request-schema.md).

## Example Usage

```ruby
token = 'token6'

scopes = 'scopes4'

trigger_id = 'trigger_id6'

result = apps_permissions_api.apps_permissions_request(
  token,
  scopes,
  trigger_id
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
| Default | Standard failure response when trigger_id is invalid | [`AppsPermissionsRequestErrorSchemaException`](../../doc/models/apps-permissions-request-error-schema-exception.md) |

