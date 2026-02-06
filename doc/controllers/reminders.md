# Reminders

```ruby
reminders_api = client.reminders
```

## Class Name

`RemindersApi`

## Methods

* [Reminders Add](../../doc/controllers/reminders.md#reminders-add)
* [Reminders Complete](../../doc/controllers/reminders.md#reminders-complete)
* [Reminders Delete](../../doc/controllers/reminders.md#reminders-delete)
* [Reminders Info](../../doc/controllers/reminders.md#reminders-info)
* [Reminders List](../../doc/controllers/reminders.md#reminders-list)


# Reminders Add

Creates a reminder.

API method documentation: [https://api.slack.com/methods/reminders.add](https://api.slack.com/methods/reminders.add)

```ruby
def reminders_add(token,
                  text,
                  time,
                  user: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `reminders:write` |
| `text` | `String` | Form, Required | The content of the reminder |
| `time` | `String` | Form, Required | When this reminder should happen: the Unix timestamp (up to five years from now), the number of seconds until the reminder (if within 24 hours), or a natural language description (Ex. "in 15 minutes," or "every Thursday") |
| `user` | `String` | Form, Optional | The user who will receive the reminder. If no user is specified, the reminder will go to user who created it. |

## Requires scope

### slackAuth

`reminders:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`RemindersAddSchema`](../../doc/models/reminders-add-schema.md).

## Example Usage

```ruby
token = 'token6'

text = 'text0'

time = 'time0'

result = reminders_api.reminders_add(
  token,
  text,
  time
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
| Default | Typical error response | [`RemindersAddErrorSchemaException`](../../doc/models/reminders-add-error-schema-exception.md) |


# Reminders Complete

Marks a reminder as complete.

API method documentation: [https://api.slack.com/methods/reminders.complete](https://api.slack.com/methods/reminders.complete)

```ruby
def reminders_complete(token: nil,
                       reminder: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Optional | Authentication token. Requires scope: `reminders:write` |
| `reminder` | `String` | Form, Optional | The ID of the reminder to be marked as complete |

## Requires scope

### slackAuth

`reminders:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`RemindersCompleteSchema`](../../doc/models/reminders-complete-schema.md).

## Example Usage

```ruby
result = reminders_api.reminders_complete

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`RemindersCompleteErrorSchemaException`](../../doc/models/reminders-complete-error-schema-exception.md) |


# Reminders Delete

Deletes a reminder.

API method documentation: [https://api.slack.com/methods/reminders.delete](https://api.slack.com/methods/reminders.delete)

```ruby
def reminders_delete(token: nil,
                     reminder: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Optional | Authentication token. Requires scope: `reminders:write` |
| `reminder` | `String` | Form, Optional | The ID of the reminder |

## Requires scope

### slackAuth

`reminders:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`RemindersDeleteSchema`](../../doc/models/reminders-delete-schema.md).

## Example Usage

```ruby
result = reminders_api.reminders_delete

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`RemindersDeleteErrorSchemaException`](../../doc/models/reminders-delete-error-schema-exception.md) |


# Reminders Info

Gets information about a reminder.

API method documentation: [https://api.slack.com/methods/reminders.info](https://api.slack.com/methods/reminders.info)

```ruby
def reminders_info(token: nil,
                   reminder: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `reminders:read` |
| `reminder` | `String` | Query, Optional | The ID of the reminder |

## Requires scope

### slackAuth

`reminders:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`RemindersInfoSchema`](../../doc/models/reminders-info-schema.md).

## Example Usage

```ruby
result = reminders_api.reminders_info

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`RemindersInfoErrorSchemaException`](../../doc/models/reminders-info-error-schema-exception.md) |


# Reminders List

Lists all reminders created by or for a given user.

API method documentation: [https://api.slack.com/methods/reminders.list](https://api.slack.com/methods/reminders.list)

```ruby
def reminders_list(token: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `reminders:read` |

## Requires scope

### slackAuth

`reminders:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`RemindersListSchema`](../../doc/models/reminders-list-schema.md).

## Example Usage

```ruby
result = reminders_api.reminders_list

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`RemindersListErrorSchemaException`](../../doc/models/reminders-list-error-schema-exception.md) |

