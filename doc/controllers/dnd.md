# Dnd

```ruby
dnd_api = client.dnd
```

## Class Name

`DndApi`

## Methods

* [Dnd End Dnd](../../doc/controllers/dnd.md#dnd-end-dnd)
* [Dnd End Snooze](../../doc/controllers/dnd.md#dnd-end-snooze)
* [Dnd Info](../../doc/controllers/dnd.md#dnd-info)
* [Dnd Set Snooze](../../doc/controllers/dnd.md#dnd-set-snooze)
* [Dnd Team Info](../../doc/controllers/dnd.md#dnd-team-info)


# Dnd End Dnd

Ends the current user's Do Not Disturb session immediately.

API method documentation: [https://api.slack.com/methods/dnd.endDnd](https://api.slack.com/methods/dnd.endDnd)

```ruby
def dnd_end_dnd(token)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `dnd:write` |

## Requires scope

### slackAuth

`dnd:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DndEndDndSchema`](../../doc/models/dnd-end-dnd-schema.md).

## Example Usage

```ruby
token = 'token6'

result = dnd_api.dnd_end_dnd(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`DndEndDndErrorSchemaException`](../../doc/models/dnd-end-dnd-error-schema-exception.md) |


# Dnd End Snooze

Ends the current user's snooze mode immediately.

API method documentation: [https://api.slack.com/methods/dnd.endSnooze](https://api.slack.com/methods/dnd.endSnooze)

```ruby
def dnd_end_snooze(token)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `dnd:write` |

## Requires scope

### slackAuth

`dnd:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DndEndSnoozeSchema`](../../doc/models/dnd-end-snooze-schema.md).

## Example Usage

```ruby
token = 'token6'

result = dnd_api.dnd_end_snooze(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`DndEndSnoozeErrorSchemaException`](../../doc/models/dnd-end-snooze-error-schema-exception.md) |


# Dnd Info

Retrieves a user's current Do Not Disturb status.

API method documentation: [https://api.slack.com/methods/dnd.info](https://api.slack.com/methods/dnd.info)

```ruby
def dnd_info(token: nil,
             user: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `dnd:read` |
| `user` | `String` | Query, Optional | User to fetch status for (defaults to current user) |

## Requires scope

### slackAuth

`dnd:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DndInfoSchema`](../../doc/models/dnd-info-schema.md).

## Example Usage

```ruby
result = dnd_api.dnd_info

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`DndInfoErrorSchemaException`](../../doc/models/dnd-info-error-schema-exception.md) |


# Dnd Set Snooze

Turns on Do Not Disturb mode for the current user, or changes its duration.

API method documentation: [https://api.slack.com/methods/dnd.setSnooze](https://api.slack.com/methods/dnd.setSnooze)

```ruby
def dnd_set_snooze(token,
                   num_minutes)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Required | Authentication token. Requires scope: `dnd:write` |
| `num_minutes` | `String` | Form, Required | Number of minutes, from now, to snooze until. |

## Requires scope

### slackAuth

`dnd:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DndSetSnoozeSchema`](../../doc/models/dnd-set-snooze-schema.md).

## Example Usage

```ruby
token = 'token6'

num_minutes = 'num_minutes0'

result = dnd_api.dnd_set_snooze(
  token,
  num_minutes
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
| Default | Typical error response | [`DndSetSnoozeErrorSchemaException`](../../doc/models/dnd-set-snooze-error-schema-exception.md) |


# Dnd Team Info

Retrieves the Do Not Disturb status for up to 50 users on a team.

API method documentation: [https://api.slack.com/methods/dnd.teamInfo](https://api.slack.com/methods/dnd.teamInfo)

```ruby
def dnd_team_info(token: nil,
                  users: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `dnd:read` |
| `users` | `String` | Query, Optional | Comma-separated list of users to fetch Do Not Disturb status for |

## Requires scope

### slackAuth

`dnd:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
result = dnd_api.dnd_team_info

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

