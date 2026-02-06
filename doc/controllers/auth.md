# Auth

```ruby
auth_api = client.auth
```

## Class Name

`AuthApi`

## Methods

* [Auth Revoke](../../doc/controllers/auth.md#auth-revoke)
* [Auth Test](../../doc/controllers/auth.md#auth-test)


# Auth Revoke

Revokes a token.

API method documentation: [https://api.slack.com/methods/auth.revoke](https://api.slack.com/methods/auth.revoke)

```ruby
def auth_revoke(token,
                test: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `none` |
| `test` | `TrueClass \| FalseClass` | Query, Optional | Setting this parameter to `1` triggers a _testing mode_ where the specified token will not actually be revoked. |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AuthRevokeSchema`](../../doc/models/auth-revoke-schema.md).

## Example Usage

```ruby
token = 'token6'

result = auth_api.auth_revoke(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`AuthRevokeErrorSchemaException`](../../doc/models/auth-revoke-error-schema-exception.md) |


# Auth Test

Checks authentication & identity.

API method documentation: [https://api.slack.com/methods/auth.test](https://api.slack.com/methods/auth.test)

```ruby
def auth_test(token)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Header, Required | Authentication token. Requires scope: `none` |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`AuthTestSuccessSchema`](../../doc/models/auth-test-success-schema.md).

## Example Usage

```ruby
token = 'token6'

result = auth_api.auth_test(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Standard failure response when used with an invalid token | [`AuthTestErrorSchemaException`](../../doc/models/auth-test-error-schema-exception.md) |

