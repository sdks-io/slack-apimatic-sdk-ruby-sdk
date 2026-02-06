# Oauth

```ruby
oauth_api = client.oauth
```

## Class Name

`OauthApi`

## Methods

* [Oauth Access](../../doc/controllers/oauth.md#oauth-access)
* [Oauth Token](../../doc/controllers/oauth.md#oauth-token)


# Oauth Access

Exchanges a temporary OAuth verifier code for an access token.

API method documentation: [https://api.slack.com/methods/oauth.access](https://api.slack.com/methods/oauth.access)

```ruby
def oauth_access(client_id: nil,
                 client_secret: nil,
                 code: nil,
                 redirect_uri: nil,
                 single_channel: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `client_id` | `String` | Query, Optional | Issued when you created your application. |
| `client_secret` | `String` | Query, Optional | Issued when you created your application. |
| `code` | `String` | Query, Optional | The `code` param returned via the OAuth callback. |
| `redirect_uri` | `String` | Query, Optional | This must match the originally submitted URI (if one was sent). |
| `single_channel` | `TrueClass \| FalseClass` | Query, Optional | Request the user to add your app only to a single channel. Only valid with a [legacy workspace app](https://api.slack.com/legacy-workspace-apps). |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
result = oauth_api.oauth_access

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


# Oauth Token

Exchanges a temporary OAuth verifier code for a workspace token.

API method documentation: [https://api.slack.com/methods/oauth.token](https://api.slack.com/methods/oauth.token)

```ruby
def oauth_token(client_id: nil,
                client_secret: nil,
                code: nil,
                redirect_uri: nil,
                single_channel: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `client_id` | `String` | Query, Optional | Issued when you created your application. |
| `client_secret` | `String` | Query, Optional | Issued when you created your application. |
| `code` | `String` | Query, Optional | The `code` param returned via the OAuth callback. |
| `redirect_uri` | `String` | Query, Optional | This must match the originally submitted URI (if one was sent). |
| `single_channel` | `TrueClass \| FalseClass` | Query, Optional | Request the user to add your app only to a single channel. |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
result = oauth_api.oauth_token

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

