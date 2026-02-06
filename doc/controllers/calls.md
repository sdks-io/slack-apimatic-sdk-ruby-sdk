# Calls

```ruby
calls_api = client.calls
```

## Class Name

`CallsApi`

## Methods

* [Calls Add](../../doc/controllers/calls.md#calls-add)
* [Calls End](../../doc/controllers/calls.md#calls-end)
* [Calls Info](../../doc/controllers/calls.md#calls-info)
* [Calls Update](../../doc/controllers/calls.md#calls-update)


# Calls Add

Registers a new Call.

API method documentation: [https://api.slack.com/methods/calls.add](https://api.slack.com/methods/calls.add)

```ruby
def calls_add(token,
              external_unique_id,
              join_url,
              external_display_id: nil,
              desktop_app_join_url: nil,
              date_start: nil,
              title: nil,
              created_by: nil,
              users: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `calls:write` |
| `external_unique_id` | `String` | Form, Required | An ID supplied by the 3rd-party Call provider. It must be unique across all Calls from that service. |
| `join_url` | `String` | Form, Required | The URL required for a client to join the Call. |
| `external_display_id` | `String` | Form, Optional | An optional, human-readable ID supplied by the 3rd-party Call provider. If supplied, this ID will be displayed in the Call object. |
| `desktop_app_join_url` | `String` | Form, Optional | When supplied, available Slack clients will attempt to directly launch the 3rd-party Call with this URL. |
| `date_start` | `Integer` | Form, Optional | Call start time in UTC UNIX timestamp format |
| `title` | `String` | Form, Optional | The name of the Call. |
| `created_by` | `String` | Form, Optional | The valid Slack user ID of the user who created this Call. When this method is called with a user token, the `created_by` field is optional and defaults to the authed user of the token. Otherwise, the field is required. |
| `users` | `String` | Form, Optional | The list of users to register as participants in the Call. [Read more on how to specify users here](/apis/calls#users). |

## Requires scope

### slackAuth

`calls:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

external_unique_id = 'external_unique_id0'

join_url = 'join_url6'

result = calls_api.calls_add(
  token,
  external_unique_id,
  join_url
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


# Calls End

Ends a Call.

API method documentation: [https://api.slack.com/methods/calls.end](https://api.slack.com/methods/calls.end)

```ruby
def calls_end(token,
              id,
              duration: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `calls:write` |
| `id` | `String` | Form, Required | `id` returned when registering the call using the [`calls.add`](/methods/calls.add) method. |
| `duration` | `Integer` | Form, Optional | Call duration in seconds |

## Requires scope

### slackAuth

`calls:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

id = 'id0'

result = calls_api.calls_end(
  token,
  id
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


# Calls Info

Returns information about a Call.

API method documentation: [https://api.slack.com/methods/calls.info](https://api.slack.com/methods/calls.info)

```ruby
def calls_info(token,
               id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `calls:read` |
| `id` | `String` | Query, Required | `id` of the Call returned by the [`calls.add`](/methods/calls.add) method. |

## Requires scope

### slackAuth

`calls:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

id = 'id0'

result = calls_api.calls_info(
  token,
  id
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


# Calls Update

Updates information about a Call.

API method documentation: [https://api.slack.com/methods/calls.update](https://api.slack.com/methods/calls.update)

```ruby
def calls_update(token,
                 id,
                 title: nil,
                 join_url: nil,
                 desktop_app_join_url: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `calls:write` |
| `id` | `String` | Form, Required | `id` returned by the [`calls.add`](/methods/calls.add) method. |
| `title` | `String` | Form, Optional | The name of the Call. |
| `join_url` | `String` | Form, Optional | The URL required for a client to join the Call. |
| `desktop_app_join_url` | `String` | Form, Optional | When supplied, available Slack clients will attempt to directly launch the 3rd-party Call with this URL. |

## Requires scope

### slackAuth

`calls:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

id = 'id0'

result = calls_api.calls_update(
  token,
  id
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

