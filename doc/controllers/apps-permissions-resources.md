# Apps Permissions Resources

```ruby
apps_permissions_resources_api = client.apps_permissions_resources
```

## Class Name

`AppsPermissionsResourcesApi`


# Apps Permissions Resources List

Returns list of resource grants this app has on a team.

API method documentation: [https://api.slack.com/methods/apps.permissions.resources.list](https://api.slack.com/methods/apps.permissions.resources.list)

```ruby
def apps_permissions_resources_list(token,
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

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AppsPermissionsResourcesListSuccessSchema`](../../doc/models/apps-permissions-resources-list-success-schema.md).

## Example Usage

```ruby
token = 'token6'

result = apps_permissions_resources_api.apps_permissions_resources_list(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`AppsPermissionsResourcesListErrorSchemaException`](../../doc/models/apps-permissions-resources-list-error-schema-exception.md) |

