# Chat Scheduled Messages

```ruby
chat_scheduled_messages_api = client.chat_scheduled_messages
```

## Class Name

`ChatScheduledMessagesApi`


# Chat Scheduled Messages List

Returns a list of scheduled messages.

API method documentation: [https://api.slack.com/methods/chat.scheduledMessages.list](https://api.slack.com/methods/chat.scheduledMessages.list)

```ruby
def chat_scheduled_messages_list(token: nil,
                                 channel: nil,
                                 latest: nil,
                                 oldest: nil,
                                 limit: nil,
                                 cursor: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Optional | Authentication token. Requires scope: `none` |
| `channel` | `String` | Query, Optional | The channel of the scheduled messages |
| `latest` | `Float` | Query, Optional | A UNIX timestamp of the latest value in the time range |
| `oldest` | `Float` | Query, Optional | A UNIX timestamp of the oldest value in the time range |
| `limit` | `Integer` | Query, Optional | Maximum number of original entries to return. |
| `cursor` | `String` | Query, Optional | For pagination purposes, this is the `cursor` value returned from a previous call to `chat.scheduledmessages.list` indicating where you want to start this call from. |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ChatScheduledMessagesListSchema`](../../doc/models/chat-scheduled-messages-list-schema.md).

## Example Usage

```ruby
result = chat_scheduled_messages_api.chat_scheduled_messages_list

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response if the channel passed is invalid | [`ChatScheduledMessagesListErrorSchemaException`](../../doc/models/chat-scheduled-messages-list-error-schema-exception.md) |

