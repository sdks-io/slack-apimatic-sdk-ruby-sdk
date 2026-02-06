# Bots

```ruby
bots_api = client.bots
```

## Class Name

`BotsApi`


# Bots Info

Gets information about a bot user.

API method documentation: [https://api.slack.com/methods/bots.info](https://api.slack.com/methods/bots.info)

```ruby
def bots_info(token,
              bot: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `users:read` |
| `bot` | `String` | Query, Optional | Bot user to get info on |

## Requires scope

### slackAuth

`users:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`BotsInfoSchema`](../../doc/models/bots-info-schema.md).

## Example Usage

```ruby
token = 'token6'

result = bots_api.bots_info(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | When no bot can be found, it returns an error. | [`BotsInfoErrorSchemaException`](../../doc/models/bots-info-error-schema-exception.md) |

