# Team

```ruby
team_api = client.team
```

## Class Name

`TeamApi`

## Methods

* [Team Access Logs](../../doc/controllers/team.md#team-access-logs)
* [Team Billable Info](../../doc/controllers/team.md#team-billable-info)
* [Team Info](../../doc/controllers/team.md#team-info)
* [Team Integration Logs](../../doc/controllers/team.md#team-integration-logs)


# Team Access Logs

Gets the access logs for the current team.

API method documentation: [https://api.slack.com/methods/team.accessLogs](https://api.slack.com/methods/team.accessLogs)

```ruby
def team_access_logs(token,
                     before: nil,
                     count: nil,
                     page: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `admin` |
| `before` | `String` | Query, Optional | End of time range of logs to include in results (inclusive). |
| `count` | `String` | Query, Optional | - |
| `page` | `String` | Query, Optional | - |

## Requires scope

### slackAuth

`admin`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`TeamAccessLogsSchema`](../../doc/models/team-access-logs-schema.md).

## Example Usage

```ruby
token = 'token6'

result = team_api.team_access_logs(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | A workspace must be on a paid plan to use this method, otherwise the `paid_only` error is thrown: | [`TeamAccessLogsErrorSchemaException`](../../doc/models/team-access-logs-error-schema-exception.md) |


# Team Billable Info

Gets billable users information for the current team.

API method documentation: [https://api.slack.com/methods/team.billableInfo](https://api.slack.com/methods/team.billableInfo)

```ruby
def team_billable_info(token,
                       user: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `admin` |
| `user` | `String` | Query, Optional | A user to retrieve the billable information for. Defaults to all users. |

## Requires scope

### slackAuth

`admin`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`DefaultSuccessTemplate`](../../doc/models/default-success-template.md).

## Example Usage

```ruby
token = 'token6'

result = team_api.team_billable_info(token)

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


# Team Info

Gets information about the current team.

API method documentation: [https://api.slack.com/methods/team.info](https://api.slack.com/methods/team.info)

```ruby
def team_info(token,
              team: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `team:read` |
| `team` | `String` | Query, Optional | Team to get info on, if omitted, will return information about the current team. Will only return team that the authenticated token is allowed to see through external shared channels |

## Requires scope

### slackAuth

`team:read`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`TeamInfoSchema`](../../doc/models/team-info-schema.md).

## Example Usage

```ruby
token = 'token6'

result = team_api.team_info(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`TeamInfoErrorSchemaException`](../../doc/models/team-info-error-schema-exception.md) |


# Team Integration Logs

Gets the integration logs for the current team.

API method documentation: [https://api.slack.com/methods/team.integrationLogs](https://api.slack.com/methods/team.integrationLogs)

```ruby
def team_integration_logs(token,
                          app_id: nil,
                          change_type: nil,
                          count: nil,
                          page: nil,
                          service_id: nil,
                          user: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `String` | Query, Required | Authentication token. Requires scope: `admin` |
| `app_id` | `String` | Query, Optional | Filter logs to this Slack app. Defaults to all logs. |
| `change_type` | `String` | Query, Optional | Filter logs with this change type. Defaults to all logs. |
| `count` | `String` | Query, Optional | - |
| `page` | `String` | Query, Optional | - |
| `service_id` | `String` | Query, Optional | Filter logs to this service. Defaults to all logs. |
| `user` | `String` | Query, Optional | Filter logs generated by this user’s actions. Defaults to all logs. |

## Requires scope

### slackAuth

`admin`

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`TeamIntegrationLogsSchema`](../../doc/models/team-integration-logs-schema.md).

## Example Usage

```ruby
token = 'token6'

result = team_api.team_integration_logs(token)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| Default | Typical error response | [`TeamIntegrationLogsErrorSchemaException`](../../doc/models/team-integration-logs-error-schema-exception.md) |

