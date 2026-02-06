# Reactions

```ruby
reactions_api = client.reactions
```

## Class Name

`ReactionsApi`

## Methods

* [Reactions Add](../../doc/controllers/reactions.md#reactions-add)
* [Reactions Get](../../doc/controllers/reactions.md#reactions-get)
* [Reactions List](../../doc/controllers/reactions.md#reactions-list)
* [Reactions Remove](../../doc/controllers/reactions.md#reactions-remove)


# Reactions Add

Adds a reaction to an item.

API method documentation: [https://api.slack.com/methods/reactions.add](https://api.slack.com/methods/reactions.add)

```ruby
def reactions_add(channel,
                  name,
                  timestamp,
                  token)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `String` | Form, Required | Channel where the message to add reaction to was posted. |
| `name` | `String` | Form, Required | Reaction (emoji) name. |
| `timestamp` | `String` | Form, Required | Timestamp of the message to add reaction to. |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `reactions:write` |

## Requires scope

### slackAuth

`reactions:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ReactionsAddSchema`](../../doc/models/reactions-add-schema.md).

## Example Usage

```ruby
channel = 'channel4'

name = 'name0'

timestamp = 'timestamp2'

token = 'token6'

result = reactions_api.reactions_add(
  channel,
  name,
  timestamp,
  token
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
| Default | Typical error response | [`ReactionsAddErrorSchemaException`](../../doc/models/reactions-add-error-schema-exception.md) |


# Reactions Get

Gets reactions for an item.

API method documentation: [https://api.slack.com/methods/reactions.get](https://api.slack.com/methods/reactions.get)

```ruby
def reactions_get(token,
                  channel: nil,
                  file: nil,
                  file_comment: nil,
                  full: nil,
                  timestamp: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `reactions:read` |
| `channel` | `String` | Query, Optional | Channel where the message to get reactions for was posted. |
| `file` | `String` | Query, Optional | File to get reactions for. |
| `file_comment` | `String` | Query, Optional | File comment to get reactions for. |
| `full` | `TrueClass \| FalseClass` | Query, Optional | If true always return the complete reaction list. |
| `timestamp` | `String` | Query, Optional | Timestamp of the message to get reactions for. |

## Requires scope

### slackAuth

`reactions:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type `Object`.

## Example Usage

```ruby
token = 'token6'

result = reactions_api.reactions_get(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response

```
{
  "file": {
    "channels": [
      "C2U7V2YA2"
    ],
    "comments_count": 1,
    "created": 1507850315,
    "groups": [],
    "id": "F7H0D7ZA4",
    "ims": [],
    "name": "computer.gif",
    "reactions": [
      {
        "count": 1,
        "name": "stuck_out_tongue_winking_eye",
        "users": [
          "U2U85N1RV"
        ]
      }
    ],
    "timestamp": 1507850315,
    "title": "computer.gif",
    "user": "U2U85N1RV"
  },
  "ok": true,
  "type": "file"
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`ReactionsGetErrorSchemaException`](../../doc/models/reactions-get-error-schema-exception.md) |


# Reactions List

Lists reactions made by a user.

API method documentation: [https://api.slack.com/methods/reactions.list](https://api.slack.com/methods/reactions.list)

```ruby
def reactions_list(token,
                   user: nil,
                   full: nil,
                   count: nil,
                   page: nil,
                   cursor: nil,
                   limit: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `reactions:read` |
| `user` | `String` | Query, Optional | Show reactions made by this user. Defaults to the authed user. |
| `full` | `TrueClass \| FalseClass` | Query, Optional | If true always return the complete reaction list. |
| `count` | `Integer` | Query, Optional | - |
| `page` | `Integer` | Query, Optional | - |
| `cursor` | `String` | Query, Optional | Parameter for pagination. Set `cursor` equal to the `next_cursor` attribute returned by the previous request's `response_metadata`. This parameter is optional, but pagination is mandatory: the default value simply fetches the first "page" of the collection. See [pagination](/docs/pagination) for more details. |
| `limit` | `Integer` | Query, Optional | The maximum number of items to return. Fewer than the requested number of items may be returned, even if the end of the list hasn't been reached. |

## Requires scope

### slackAuth

`reactions:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ReactionsListSchema`](../../doc/models/reactions-list-schema.md).

## Example Usage

```ruby
token = 'token6'

result = reactions_api.reactions_list(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`ReactionsListErrorSchemaException`](../../doc/models/reactions-list-error-schema-exception.md) |


# Reactions Remove

Removes a reaction from an item.

API method documentation: [https://api.slack.com/methods/reactions.remove](https://api.slack.com/methods/reactions.remove)

```ruby
def reactions_remove(token,
                     name,
                     file: nil,
                     file_comment: nil,
                     channel: nil,
                     timestamp: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `reactions:write` |
| `name` | `String` | Form, Required | Reaction (emoji) name. |
| `file` | `String` | Form, Optional | File to remove reaction from. |
| `file_comment` | `String` | Form, Optional | File comment to remove reaction from. |
| `channel` | `String` | Form, Optional | Channel where the message to remove reaction from was posted. |
| `timestamp` | `String` | Form, Optional | Timestamp of the message to remove reaction from. |

## Requires scope

### slackAuth

`reactions:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ReactionsRemoveSchema`](../../doc/models/reactions-remove-schema.md).

## Example Usage

```ruby
token = 'token6'

name = 'name0'

result = reactions_api.reactions_remove(
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
| Default | Typical error response | [`ReactionsRemoveErrorSchemaException`](../../doc/models/reactions-remove-error-schema-exception.md) |

