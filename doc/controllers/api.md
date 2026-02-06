# Api

```ruby
api = client.api
```

## Class Name

`Api`


# Api Test

Checks API calling code.

API method documentation: [https://api.slack.com/methods/api.test](https://api.slack.com/methods/api.test)

```ruby
def api_test(error: nil,
             foo: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | `String` | Query, Optional | Error response to return |
| `foo` | `String` | Query, Optional | example property to return |

## Requires scope

### slackAuth

`none`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ApiTestSuccessSchema`](../../doc/models/api-test-success-schema.md).

## Example Usage

```ruby
result = api.api_test

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Artificial error response | [`ApiTestErrorSchemaException`](../../doc/models/api-test-error-schema-exception.md) |

