# Rtm

```ruby
rtm_api = client.rtm
```

## Class Name

`RtmApi`


# Rtm Connect

Starts a Real Time Messaging session.

API method documentation: [https://api.slack.com/methods/rtm.connect](https://api.slack.com/methods/rtm.connect)

```ruby
def rtm_connect(token,
                batch_presence_aware: nil,
                presence_sub: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `rtm:stream` |
| `batch_presence_aware` | `TrueClass \| FalseClass` | Query, Optional | Batch presence deliveries via subscription. Enabling changes the shape of `presence_change` events. See [batch presence](/docs/presence-and-status#batching). |
| `presence_sub` | `TrueClass \| FalseClass` | Query, Optional | Only deliver presence events when requested by subscription. See [presence subscriptions](/docs/presence-and-status#subscriptions). |

## Requires scope

### slackAuth

`rtm:stream`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`RtmConnectSchema`](../../doc/models/rtm-connect-schema.md).

## Example Usage

```ruby
token = 'token6'

result = rtm_api.rtm_connect(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`RtmConnectErrorSchemaException`](../../doc/models/rtm-connect-error-schema-exception.md) |

