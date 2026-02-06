# Team Profile

```ruby
team_profile_api = client.team_profile
```

## Class Name

`TeamProfileApi`


# Team Profile Get

Retrieve a team's profile.

API method documentation: [https://api.slack.com/methods/team.profile.get](https://api.slack.com/methods/team.profile.get)

```ruby
def team_profile_get(token,
                     visibility: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `users.profile:read` |
| `visibility` | `String` | Query, Optional | Filter by visibility. |

## Requires scope

### slackAuth

`users.profile:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`TeamProfileGetSuccessSchema`](../../doc/models/team-profile-get-success-schema.md).

## Example Usage

```ruby
token = 'token6'

result = team_profile_api.team_profile_get(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`TeamProfileGetErrorSchemaException`](../../doc/models/team-profile-get-error-schema-exception.md) |

