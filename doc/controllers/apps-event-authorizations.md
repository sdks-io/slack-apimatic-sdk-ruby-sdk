# Apps Event Authorizations

```ruby
apps_event_authorizations_api = client.apps_event_authorizations
```

## Class Name

`AppsEventAuthorizationsApi`


# Apps Event Authorizations List

Get a list of authorizations for the given event context. Each authorization represents an app installation that the event is visible to.

API method documentation: [https://api.slack.com/methods/apps.event.authorizations.list](https://api.slack.com/methods/apps.event.authorizations.list)

```ruby
def apps_event_authorizations_list(token,
                                   event_context,
                                   cursor: nil,
                                   limit: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `authorizations:read` |
| `event_context` | `String` | Query, Required | - |
| `cursor` | `String` | Query, Optional | - |
| `limit` | `Integer` | Query, Optional | - |

## Requires scope

### slackAuth

`authorizations:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

event_context = 'event_context0'

result = apps_event_authorizations_api.apps_event_authorizations_list(
  token,
  event_context
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
| Default | Typical error response | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |

