# Admin Apps

```ruby
admin_apps_api = client.admin_apps
```

## Class Name

`AdminAppsApi`

## Methods

* [Admin Apps Approve](../../doc/controllers/admin-apps.md#admin-apps-approve)
* [Admin Apps Restrict](../../doc/controllers/admin-apps.md#admin-apps-restrict)


# Admin Apps Approve

Approve an app for installation on a workspace.

API method documentation: [https://api.slack.com/methods/admin.apps.approve](https://api.slack.com/methods/admin.apps.approve)

```ruby
def admin_apps_approve(token,
                       app_id: nil,
                       request_id: nil,
                       team_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.apps:write` |
| `app_id` | `String` | Form, Optional | The id of the app to approve. |
| `request_id` | `String` | Form, Optional | The id of the request to approve. |
| `team_id` | `String` | Form, Optional | - |

## Requires scope

### slackAuth

`admin.apps:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

result = admin_apps_api.admin_apps_approve(token)

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


# Admin Apps Restrict

Restrict an app for installation on a workspace.

API method documentation: [https://api.slack.com/methods/admin.apps.restrict](https://api.slack.com/methods/admin.apps.restrict)

```ruby
def admin_apps_restrict(token,
                        app_id: nil,
                        request_id: nil,
                        team_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `admin.apps:write` |
| `app_id` | `String` | Form, Optional | The id of the app to restrict. |
| `request_id` | `String` | Form, Optional | The id of the request to restrict. |
| `team_id` | `String` | Form, Optional | - |

## Requires scope

### slackAuth

`admin.apps:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

result = admin_apps_api.admin_apps_restrict(token)

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

