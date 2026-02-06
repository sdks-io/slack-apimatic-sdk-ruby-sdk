# Files Comments

```ruby
files_comments_api = client.files_comments
```

## Class Name

`FilesCommentsApi`


# Files Comments Delete

Deletes an existing comment on a file.

API method documentation: [https://api.slack.com/methods/files.comments.delete](https://api.slack.com/methods/files.comments.delete)

```ruby
def files_comments_delete(token: nil,
                          file: nil,
                          id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Optional | Authentication token. Requires scope: `files:write:user` |
| `file` | `String` | Form, Optional | File to delete a comment from. |
| `id` | `String` | Form, Optional | The comment to delete. |

## Requires scope

### slackAuth

`files:write:user`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`FilesCommentsDeleteSchema`](../../doc/models/files-comments-delete-schema.md).

## Example Usage

```ruby
result = files_comments_api.files_comments_delete

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Standard failure response when used with an invalid token | [`FilesCommentsDeleteErrorSchemaException`](../../doc/models/files-comments-delete-error-schema-exception.md) |

