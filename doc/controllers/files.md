# Files

```ruby
files_api = client.files
```

## Class Name

`FilesApi`

## Methods

* [Files Delete](../../doc/controllers/files.md#files-delete)
* [Files Info](../../doc/controllers/files.md#files-info)
* [Files List](../../doc/controllers/files.md#files-list)
* [Files Revoke Public URL](../../doc/controllers/files.md#files-revoke-public-url)
* [Files Shared Public URL](../../doc/controllers/files.md#files-shared-public-url)
* [Files Upload](../../doc/controllers/files.md#files-upload)


# Files Delete

Deletes a file.

API method documentation: [https://api.slack.com/methods/files.delete](https://api.slack.com/methods/files.delete)

```ruby
def files_delete(token: nil,
                 file: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Optional | Authentication token. Requires scope: `files:write:user` |
| `file` | `String` | Form, Optional | ID of file to delete. |

## Requires scope

### slackAuth

`files:write:user`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`FilesDeleteSchema`](../../doc/models/files-delete-schema.md).

## Example Usage

```ruby
result = files_api.files_delete

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`FilesDeleteErrorSchemaException`](../../doc/models/files-delete-error-schema-exception.md) |


# Files Info

Gets information about a file.

API method documentation: [https://api.slack.com/methods/files.info](https://api.slack.com/methods/files.info)

```ruby
def files_info(token: nil,
               file: nil,
               count: nil,
               page: nil,
               limit: nil,
               cursor: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `files:read` |
| `file` | `String` | Query, Optional | Specify a file by providing its ID. |
| `count` | `String` | Query, Optional | - |
| `page` | `String` | Query, Optional | - |
| `limit` | `Integer` | Query, Optional | The maximum number of items to return. Fewer than the requested number of items may be returned, even if the end of the list hasn't been reached. |
| `cursor` | `String` | Query, Optional | Parameter for pagination. File comments are paginated for a single file. Set `cursor` equal to the `next_cursor` attribute returned by the previous request's `response_metadata`. This parameter is optional, but pagination is mandatory: the default value simply fetches the first "page" of the collection of comments. |

## Requires scope

### slackAuth

`files:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`FilesInfoSchema`](../../doc/models/files-info-schema.md).

## Example Usage

```ruby
result = files_api.files_info

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`FilesInfoErrorSchemaException`](../../doc/models/files-info-error-schema-exception.md) |


# Files List

List for a team, in a channel, or from a user with applied filters.

API method documentation: [https://api.slack.com/methods/files.list](https://api.slack.com/methods/files.list)

```ruby
def files_list(token: nil,
               user: nil,
               channel: nil,
               ts_from: nil,
               ts_to: nil,
               types: nil,
               count: nil,
               page: nil,
               show_files_hidden_by_limit: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `files:read` |
| `user` | `String` | Query, Optional | Filter files created by a single user. |
| `channel` | `String` | Query, Optional | Filter files appearing in a specific channel, indicated by its ID. |
| `ts_from` | `Float` | Query, Optional | Filter files created after this timestamp (inclusive). |
| `ts_to` | `Float` | Query, Optional | Filter files created before this timestamp (inclusive). |
| `types` | `String` | Query, Optional | Filter files by type ([see below](#file_types)). You can pass multiple values in the types argument, like `types=spaces,snippets`.The default value is `all`, which does not filter the list. |
| `count` | `String` | Query, Optional | - |
| `page` | `String` | Query, Optional | - |
| `show_files_hidden_by_limit` | `TrueClass \| FalseClass` | Query, Optional | Show truncated file info for files hidden due to being too old, and the team who owns the file being over the file limit. |

## Requires scope

### slackAuth

`files:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`FilesListSchema`](../../doc/models/files-list-schema.md).

## Example Usage

```ruby
result = files_api.files_list

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`FilesListErrorSchemaException`](../../doc/models/files-list-error-schema-exception.md) |


# Files Revoke Public URL

Revokes public/external sharing access for a file

API method documentation: [https://api.slack.com/methods/files.revokePublicURL](https://api.slack.com/methods/files.revokePublicURL)

```ruby
def files_revoke_public_url(token: nil,
                            file: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Optional | Authentication token. Requires scope: `files:write:user` |
| `file` | `String` | Form, Optional | File to revoke |

## Requires scope

### slackAuth

`files:write:user`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`FilesRevokePublicUrlSchema`](../../doc/models/files-revoke-public-url-schema.md).

## Example Usage

```ruby
result = files_api.files_revoke_public_url

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`FilesRevokePublicUrlErrorSchemaException`](../../doc/models/files-revoke-public-url-error-schema-exception.md) |


# Files Shared Public URL

Enables a file for public/external sharing.

API method documentation: [https://api.slack.com/methods/files.sharedPublicURL](https://api.slack.com/methods/files.sharedPublicURL)

```ruby
def files_shared_public_url(token: nil,
                            file: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Optional | Authentication token. Requires scope: `files:write:user` |
| `file` | `String` | Form, Optional | File to share |

## Requires scope

### slackAuth

`files:write:user`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`FilesSharedPublicUrlSchema`](../../doc/models/files-shared-public-url-schema.md).

## Example Usage

```ruby
result = files_api.files_shared_public_url

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`FilesSharedPublicUrlErrorSchemaException`](../../doc/models/files-shared-public-url-error-schema-exception.md) |


# Files Upload

Uploads or creates a file.

API method documentation: [https://api.slack.com/methods/files.upload](https://api.slack.com/methods/files.upload)

```ruby
def files_upload(token: nil,
                 file: nil,
                 content: nil,
                 filetype: nil,
                 filename: nil,
                 title: nil,
                 initial_comment: nil,
                 channels: nil,
                 thread_ts: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Optional | Authentication token. Requires scope: `files:write:user` |
| `file` | `String` | Form, Optional | File contents via `multipart/form-data`. If omitting this parameter, you must submit `content`. |
| `content` | `String` | Form, Optional | File contents via a POST variable. If omitting this parameter, you must provide a `file`. |
| `filetype` | `String` | Form, Optional | A [file type](/types/file#file_types) identifier. |
| `filename` | `String` | Form, Optional | Filename of file. |
| `title` | `String` | Form, Optional | Title of file. |
| `initial_comment` | `String` | Form, Optional | The message text introducing the file in specified `channels`. |
| `channels` | `String` | Form, Optional | Comma-separated list of channel names or IDs where the file will be shared. |
| `thread_ts` | `Float` | Form, Optional | Provide another message's `ts` value to upload this file as a reply. Never use a reply's `ts` value; use its parent instead. |

## Requires scope

### slackAuth

`files:write:user`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`FilesUploadSchema`](../../doc/models/files-upload-schema.md).

## Example Usage

```ruby
result = files_api.files_upload

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`FilesUploadErrorSchemaException`](../../doc/models/files-upload-error-schema-exception.md) |

