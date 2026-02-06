# Search

```ruby
search_api = client.search
```

## Class Name

`SearchApi`


# Search Messages

Searches for messages matching a query.

API method documentation: [https://api.slack.com/methods/search.messages](https://api.slack.com/methods/search.messages)

```ruby
def search_messages(token,
                    query,
                    count: nil,
                    highlight: nil,
                    page: nil,
                    sort: nil,
                    sort_dir: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `search:read` |
| `query` | `String` | Query, Required | Search query. |
| `count` | `Integer` | Query, Optional | Pass the number of results you want per "page". Maximum of `100`. |
| `highlight` | `TrueClass \| FalseClass` | Query, Optional | Pass a value of `true` to enable query highlight markers (see below). |
| `page` | `Integer` | Query, Optional | - |
| `sort` | `String` | Query, Optional | Return matches sorted by either `score` or `timestamp`. |
| `sort_dir` | `String` | Query, Optional | Change sort direction to ascending (`asc`) or descending (`desc`). |

## Requires scope

### slackAuth

`search:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

query = 'query0'

result = search_api.search_messages(
  token,
  query
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

