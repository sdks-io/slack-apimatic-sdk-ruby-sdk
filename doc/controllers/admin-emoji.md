# Admin Emoji

```ruby
admin_emoji_api = client.admin_emoji
```

## Class Name

`AdminEmojiApi`

## Methods

* [Admin Emoji Add](../../doc/controllers/admin-emoji.md#admin-emoji-add)
* [Admin Emoji Add Alias](../../doc/controllers/admin-emoji.md#admin-emoji-add-alias)
* [Admin Emoji List](../../doc/controllers/admin-emoji.md#admin-emoji-list)
* [Admin Emoji Remove](../../doc/controllers/admin-emoji.md#admin-emoji-remove)
* [Admin Emoji Rename](../../doc/controllers/admin-emoji.md#admin-emoji-rename)


# Admin Emoji Add

Add an emoji.

API method documentation: [https://api.slack.com/methods/admin.emoji.add](https://api.slack.com/methods/admin.emoji.add)

```ruby
def admin_emoji_add(token,
                    name,
                    url)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Required | Authentication token. Requires scope: `admin.teams:write` |
| `name` | `String` | Form, Required | The name of the emoji to be removed. Colons (`:myemoji:`) around the value are not required, although they may be included. |
| `url` | `String` | Form, Required | The URL of a file to use as an image for the emoji. Square images under 128KB and with transparent backgrounds work best. |

## Requires scope

### slackAuth

`admin.teams:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

name = 'name0'

url = 'url4'

result = admin_emoji_api.admin_emoji_add(
  token,
  name,
  url
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


# Admin Emoji Add Alias

Add an emoji alias.

API method documentation: [https://api.slack.com/methods/admin.emoji.addAlias](https://api.slack.com/methods/admin.emoji.addAlias)

```ruby
def admin_emoji_add_alias(token,
                          name,
                          alias_for)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Required | Authentication token. Requires scope: `admin.teams:write` |
| `name` | `String` | Form, Required | The name of the emoji to be aliased. Colons (`:myemoji:`) around the value are not required, although they may be included. |
| `alias_for` | `String` | Form, Required | The alias of the emoji. |

## Requires scope

### slackAuth

`admin.teams:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

name = 'name0'

alias_for = 'alias_for4'

result = admin_emoji_api.admin_emoji_add_alias(
  token,
  name,
  alias_for
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


# Admin Emoji List

List emoji for an Enterprise Grid organization.

API method documentation: [https://api.slack.com/methods/admin.emoji.list](https://api.slack.com/methods/admin.emoji.list)

```ruby
def admin_emoji_list(token,
                     cursor: nil,
                     limit: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `admin.teams:read` |
| `cursor` | `String` | Query, Optional | Set `cursor` to `next_cursor` returned by the previous call to list items in the next page |
| `limit` | `Integer` | Query, Optional | The maximum number of items to return. Must be between 1 - 1000 both inclusive. |

## Requires scope

### slackAuth

`admin.teams:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

result = admin_emoji_api.admin_emoji_list(token)

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


# Admin Emoji Remove

Remove an emoji across an Enterprise Grid organization

API method documentation: [https://api.slack.com/methods/admin.emoji.remove](https://api.slack.com/methods/admin.emoji.remove)

```ruby
def admin_emoji_remove(token,
                       name)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Required | Authentication token. Requires scope: `admin.teams:write` |
| `name` | `String` | Form, Required | The name of the emoji to be removed. Colons (`:myemoji:`) around the value are not required, although they may be included. |

## Requires scope

### slackAuth

`admin.teams:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

name = 'name0'

result = admin_emoji_api.admin_emoji_remove(
  token,
  name
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


# Admin Emoji Rename

Rename an emoji.

API method documentation: [https://api.slack.com/methods/admin.emoji.rename](https://api.slack.com/methods/admin.emoji.rename)

```ruby
def admin_emoji_rename(token,
                       name,
                       new_name)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Required | Authentication token. Requires scope: `admin.teams:write` |
| `name` | `String` | Form, Required | The name of the emoji to be renamed. Colons (`:myemoji:`) around the value are not required, although they may be included. |
| `new_name` | `String` | Form, Required | The new name of the emoji. |

## Requires scope

### slackAuth

`admin.teams:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

name = 'name0'

new_name = 'new_name8'

result = admin_emoji_api.admin_emoji_rename(
  token,
  name,
  new_name
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

