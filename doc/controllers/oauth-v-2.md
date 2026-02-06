# Oauth V 2

```ruby
oauth_v2_api = client.oauth_v2
```

## Class Name

`OauthV2Api`


# Oauth V 2 Access

Exchanges a temporary OAuth verifier code for an access token.

API method documentation: [https://api.slack.com/methods/oauth.v2.access](https://api.slack.com/methods/oauth.v2.access)

```ruby
def oauth_v2_access(code,
                    client_id: nil,
                    client_secret: nil,
                    redirect_uri: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | `String` | Query, Required | The `code` param returned via the OAuth callback. |
| `client_id` | `String` | Query, Optional | Issued when you created your application. |
| `client_secret` | `String` | Query, Optional | Issued when you created your application. |
| `redirect_uri` | `String` | Query, Optional | This must match the originally submitted URI (if one was sent). |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
code = 'code8'

result = oauth_v2_api.oauth_v2_access(code)

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

