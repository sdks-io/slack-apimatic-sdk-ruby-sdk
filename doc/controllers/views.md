# Views

```ruby
views_api = client.views
```

## Class Name

`ViewsApi`

## Methods

* [Views Open](../../doc/controllers/views.md#views-open)
* [Views Publish](../../doc/controllers/views.md#views-publish)
* [Views Push](../../doc/controllers/views.md#views-push)
* [Views Update](../../doc/controllers/views.md#views-update)


# Views Open

Open a view for a user.

API method documentation: [https://api.slack.com/methods/views.open](https://api.slack.com/methods/views.open)

```ruby
def views_open(token,
               trigger_id,
               view)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `none` |
| `trigger_id` | `String` | Query, Required | Exchange a trigger to post to the user. |
| `view` | `String` | Query, Required | A [view payload](/reference/surfaces/views). This must be a JSON-encoded string. |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

trigger_id = 'trigger_id6'

view = 'view2'

result = views_api.views_open(
  token,
  trigger_id,
  view
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
| Default | Typical error response, before getting to any possible validation errors. | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |


# Views Publish

Publish a static view for a User.

API method documentation: [https://api.slack.com/methods/views.publish](https://api.slack.com/methods/views.publish)

```ruby
def views_publish(token,
                  user_id,
                  view,
                  hash: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `none` |
| `user_id` | `String` | Query, Required | `id` of the user you want publish a view to. |
| `view` | `String` | Query, Required | A [view payload](/reference/surfaces/views). This must be a JSON-encoded string. |
| `hash` | `String` | Query, Optional | A string that represents view state to protect against possible race conditions. |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

user_id = 'user_id8'

view = 'view2'

result = views_api.views_publish(
  token,
  user_id,
  view
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
| Default | Typical error response, before getting to any possible validation errors. | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |


# Views Push

Push a view onto the stack of a root view.

API method documentation: [https://api.slack.com/methods/views.push](https://api.slack.com/methods/views.push)

```ruby
def views_push(token,
               trigger_id,
               view)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `none` |
| `trigger_id` | `String` | Query, Required | Exchange a trigger to post to the user. |
| `view` | `String` | Query, Required | A [view payload](/reference/surfaces/views). This must be a JSON-encoded string. |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

trigger_id = 'trigger_id6'

view = 'view2'

result = views_api.views_push(
  token,
  trigger_id,
  view
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
| Default | Typical error response. | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |


# Views Update

Update an existing view.

API method documentation: [https://api.slack.com/methods/views.update](https://api.slack.com/methods/views.update)

```ruby
def views_update(token,
                 view_id: nil,
                 external_id: nil,
                 view: nil,
                 hash: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `none` |
| `view_id` | `String` | Query, Optional | A unique identifier of the view to be updated. Either `view_id` or `external_id` is required. |
| `external_id` | `String` | Query, Optional | A unique identifier of the view set by the developer. Must be unique for all views on a team. Max length of 255 characters. Either `view_id` or `external_id` is required. |
| `view` | `String` | Query, Optional | A [view object](/reference/surfaces/views). This must be a JSON-encoded string. |
| `hash` | `String` | Query, Optional | A string that represents view state to protect against possible race conditions. |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

result = views_api.views_update(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response. | [`DefaultErrorTemplateException`](../../doc/models/default-error-template-exception.md) |

