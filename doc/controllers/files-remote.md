# Files Remote

```ruby
files_remote_api = client.files_remote
```

## Class Name

`FilesRemoteApi`

## Methods

* [Files Remote Add](../../doc/controllers/files-remote.md#files-remote-add)
* [Files Remote Info](../../doc/controllers/files-remote.md#files-remote-info)
* [Files Remote List](../../doc/controllers/files-remote.md#files-remote-list)
* [Files Remote Remove](../../doc/controllers/files-remote.md#files-remote-remove)
* [Files Remote Share](../../doc/controllers/files-remote.md#files-remote-share)
* [Files Remote Update](../../doc/controllers/files-remote.md#files-remote-update)


# Files Remote Add

Adds a file from a remote service

API method documentation: [https://api.slack.com/methods/files.remote.add](https://api.slack.com/methods/files.remote.add)

```ruby
def files_remote_add(token: nil,
                     external_id: nil,
                     title: nil,
                     filetype: nil,
                     external_url: nil,
                     preview_image: nil,
                     indexable_file_contents: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Optional | Authentication token. Requires scope: `remote_files:write` |
| `external_id` | `String` | Form, Optional | Creator defined GUID for the file. |
| `title` | `String` | Form, Optional | Title of the file being shared. |
| `filetype` | `String` | Form, Optional | type of file |
| `external_url` | `String` | Form, Optional | URL of the remote file. |
| `preview_image` | `String` | Form, Optional | Preview of the document via `multipart/form-data`. |
| `indexable_file_contents` | `String` | Form, Optional | A text file (txt, pdf, doc, etc.) containing textual search terms that are used to improve discovery of the remote file. |

## Requires scope

### slackAuth

`remote_files:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
result = files_remote_api.files_remote_add

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


# Files Remote Info

Retrieve information about a remote file added to Slack

API method documentation: [https://api.slack.com/methods/files.remote.info](https://api.slack.com/methods/files.remote.info)

```ruby
def files_remote_info(token: nil,
                      file: nil,
                      external_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `remote_files:read` |
| `file` | `String` | Query, Optional | Specify a file by providing its ID. |
| `external_id` | `String` | Query, Optional | Creator defined GUID for the file. |

## Requires scope

### slackAuth

`remote_files:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
result = files_remote_api.files_remote_info

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


# Files Remote List

Retrieve information about a remote file added to Slack

API method documentation: [https://api.slack.com/methods/files.remote.list](https://api.slack.com/methods/files.remote.list)

```ruby
def files_remote_list(token: nil,
                      channel: nil,
                      ts_from: nil,
                      ts_to: nil,
                      limit: nil,
                      cursor: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `remote_files:read` |
| `channel` | `String` | Query, Optional | Filter files appearing in a specific channel, indicated by its ID. |
| `ts_from` | `Float` | Query, Optional | Filter files created after this timestamp (inclusive). |
| `ts_to` | `Float` | Query, Optional | Filter files created before this timestamp (inclusive). |
| `limit` | `Integer` | Query, Optional | The maximum number of items to return. |
| `cursor` | `String` | Query, Optional | Paginate through collections of data by setting the `cursor` parameter to a `next_cursor` attribute returned by a previous request's `response_metadata`. Default value fetches the first "page" of the collection. |

## Requires scope

### slackAuth

`remote_files:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
result = files_remote_api.files_remote_list

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


# Files Remote Remove

Remove a remote file.

API method documentation: [https://api.slack.com/methods/files.remote.remove](https://api.slack.com/methods/files.remote.remove)

```ruby
def files_remote_remove(token: nil,
                        file: nil,
                        external_id: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Optional | Authentication token. Requires scope: `remote_files:write` |
| `file` | `String` | Form, Optional | Specify a file by providing its ID. |
| `external_id` | `String` | Form, Optional | Creator defined GUID for the file. |

## Requires scope

### slackAuth

`remote_files:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
result = files_remote_api.files_remote_remove

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


# Files Remote Share

Share a remote file into a channel.

API method documentation: [https://api.slack.com/methods/files.remote.share](https://api.slack.com/methods/files.remote.share)

```ruby
def files_remote_share(token: nil,
                       file: nil,
                       external_id: nil,
                       channels: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Optional | Authentication token. Requires scope: `remote_files:share` |
| `file` | `String` | Query, Optional | Specify a file registered with Slack by providing its ID. Either this field or `external_id` or both are required. |
| `external_id` | `String` | Query, Optional | The globally unique identifier (GUID) for the file, as set by the app registering the file with Slack.  Either this field or `file` or both are required. |
| `channels` | `String` | Query, Optional | Comma-separated list of channel IDs where the file will be shared. |

## Requires scope

### slackAuth

`remote_files:share`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
result = files_remote_api.files_remote_share

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


# Files Remote Update

Updates an existing remote file.

API method documentation: [https://api.slack.com/methods/files.remote.update](https://api.slack.com/methods/files.remote.update)

```ruby
def files_remote_update(token: nil,
                        file: nil,
                        external_id: nil,
                        title: nil,
                        filetype: nil,
                        external_url: nil,
                        preview_image: nil,
                        indexable_file_contents: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Form, Optional | Authentication token. Requires scope: `remote_files:write` |
| `file` | `String` | Form, Optional | Specify a file by providing its ID. |
| `external_id` | `String` | Form, Optional | Creator defined GUID for the file. |
| `title` | `String` | Form, Optional | Title of the file being shared. |
| `filetype` | `String` | Form, Optional | type of file |
| `external_url` | `String` | Form, Optional | URL of the remote file. |
| `preview_image` | `String` | Form, Optional | Preview of the document via `multipart/form-data`. |
| `indexable_file_contents` | `String` | Form, Optional | File containing contents that can be used to improve searchability for the remote file. |

## Requires scope

### slackAuth

`remote_files:write`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
result = files_remote_api.files_remote_update

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

