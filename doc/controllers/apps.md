# Apps

```ruby
apps_api = client.apps
```

## Class Name

`AppsApi`


# Apps Uninstall

Uninstalls your app from a workspace.

API method documentation: [https://api.slack.com/methods/apps.uninstall](https://api.slack.com/methods/apps.uninstall)

```ruby
def apps_uninstall(token: nil,
                   client_id: nil,
                   client_secret: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `none` |
| `client_id` | `String` | Query, Optional | Issued when you created your application. |
| `client_secret` | `String` | Query, Optional | Issued when you created your application. |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AppsUninstallSchema`](../../doc/models/apps-uninstall-schema.md).

## Example Usage

```ruby
result = apps_api.apps_uninstall

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`AppsUninstallErrorSchemaException`](../../doc/models/apps-uninstall-error-schema-exception.md) |

