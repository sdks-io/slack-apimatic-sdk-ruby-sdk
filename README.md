
# Getting Started with Slack Web API

## Introduction

One way to interact with the Slack platform is its HTTP RPC-based Web API, a collection of methods requiring OAuth 2.0-based user, bot, or workspace tokens blessed with related OAuth scopes.

Learn more about the Slack Web API: [https://api.slack.com/web](https://api.slack.com/web)

## Install the Package

Install the gem from the command line:

```bash
gem install slack-apimatic-sdk-sdk -v 1.0.1
```

Or add the gem to your Gemfile and run `bundle`:

```ruby
gem 'slack-apimatic-sdk-sdk', '1.0.1'
```

For additional gem details, see the [RubyGems page for the slack-apimatic-sdk-sdk gem](https://rubygems.org/gems/slack-apimatic-sdk-sdk/versions/1.0.1).

## IRB Console Usage

You can explore the SDK interactively using IRB in two ways

### 1. Use IRB with Installed Gem

Open your system terminal (Command Prompt, Git Bash or macOS Terminal) and type the following command to start the irb console.

```bash
irb
```

Now you can load the SDK in the IRB

```ruby
require 'slack_web_api'
include SlackWebApi
```

### 2. Use IRB within SDK

Open your system terminal (Command Prompt, Git Bash or macOS Terminal) and navigate to the root folder of SDK.

```
cd path/to/slack_web_api
```

Now you can start the preconfigured irb console by running the following command

```bash
ruby bin/console
```

**_Note:_** This automatically loads the SDK from lib/

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| connection | `Faraday::Connection` | The Faraday connection object passed by the SDK user for making requests |
| adapter | `Faraday::Adapter` | The Faraday adapter object passed by the SDK user for performing http requests |
| timeout | `Float` | The value to use for connection timeout. <br> **Default: 30** |
| max_retries | `Integer` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| retry_interval | `Float` | Pause in seconds between retries. <br> **Default: 1** |
| backoff_factor | `Float` | The amount to multiply each successive retry's interval amount by in order to provide backoff. <br> **Default: 2** |
| retry_statuses | `Array` | A list of HTTP statuses to retry. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array` | A list of HTTP methods to retry. <br> **Default: %i[get put]** |
| http_callback | `HttpCallBack` | The Http CallBack allows defining callables for pre and post API calls. |
| proxy_settings | [`ProxySettings`](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/proxy-settings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/logging-configuration.md) | The SDK logging configuration for API calls |
| authorization_code_auth_credentials | [`AuthorizationCodeAuthCredentials`](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/auth/oauth-2-authorization-code-grant.md) | The credential object for OAuth 2 Authorization Code Grant |

The API client can be initialized as follows:

### Code-Based Client Initialization

```ruby
require 'slack_web_api'
include SlackWebApi

client = Client.new(
  authorization_code_auth_credentials: AuthorizationCodeAuthCredentials.new(
    oauth_client_id: 'OAuthClientId',
    oauth_client_secret: 'OAuthClientSecret',
    oauth_redirect_uri: 'OAuthRedirectUri',
    oauth_scopes: [
      OauthScope::ADMIN,
      OauthScope::ADMIN_APPSREAD
    ]
  ),
  environment: Environment::PRODUCTION,
  logging_configuration: LoggingConfiguration.new(
    log_level: Logger::INFO,
    request_logging_config: RequestLoggingConfiguration.new(
      log_body: true
    ),
    response_logging_config: ResponseLoggingConfiguration.new(
      log_headers: true
    )
  )
)
```

### Environment-Based Client Initialization

```ruby
require 'slack_web_api'
include SlackWebApi

# Create client from environment
client = Client.from_env
```

See the [`Environment-Based Client Initialization`](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/environment-based-client-initialization.md) section for details.

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** |

## Authorization

This API uses the following authentication schemes.

* [`slackAuth (OAuth 2 Authorization Code Grant)`](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/auth/oauth-2-authorization-code-grant.md)

## List of APIs

* [Admin Apps](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-apps.md)
* [Admin Apps Approved](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-apps-approved.md)
* [Admin Apps Requests](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-apps-requests.md)
* [Admin Apps Restricted](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-apps-restricted.md)
* [Admin Conversations](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-conversations.md)
* [Admin Conversations Ekm](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-conversations-ekm.md)
* [Admin Conversations Restrict Access](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-conversations-restrict-access.md)
* [Admin Emoji](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-emoji.md)
* [Admin Invite Requests](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-invite-requests.md)
* [Admin Invite Requests Approved](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-invite-requests-approved.md)
* [Admin Invite Requests Denied](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-invite-requests-denied.md)
* [Admin Teams Admins](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-teams-admins.md)
* [Admin Teams](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-teams.md)
* [Admin Teams Owners](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-teams-owners.md)
* [Admin Teams Settings](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-teams-settings.md)
* [Admin Usergroups](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-usergroups.md)
* [Admin Users](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-users.md)
* [Admin Users Session](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/admin-users-session.md)
* [Api](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/api.md)
* [Apps Event Authorizations](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/apps-event-authorizations.md)
* [Apps Permissions](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/apps-permissions.md)
* [Apps Permissions Resources](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/apps-permissions-resources.md)
* [Apps Permissions Scopes](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/apps-permissions-scopes.md)
* [Apps Permissions Users](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/apps-permissions-users.md)
* [Apps](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/apps.md)
* [Auth](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/auth.md)
* [Bots](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/bots.md)
* [Calls](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/calls.md)
* [Calls Participants](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/calls-participants.md)
* [Chat](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/chat.md)
* [Chat Scheduled Messages](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/chat-scheduled-messages.md)
* [Conversations](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/conversations.md)
* [Dialog](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/dialog.md)
* [Dnd](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/dnd.md)
* [Emoji](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/emoji.md)
* [Files Comments](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/files-comments.md)
* [Files](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/files.md)
* [Files Remote](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/files-remote.md)
* [Migration](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/migration.md)
* [Oauth](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/oauth.md)
* [Oauth V 2](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/oauth-v-2.md)
* [Pins](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/pins.md)
* [Reactions](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/reactions.md)
* [Reminders](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/reminders.md)
* [Rtm](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/rtm.md)
* [Search](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/search.md)
* [Stars](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/stars.md)
* [Team](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/team.md)
* [Team Profile](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/team-profile.md)
* [Usergroups](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/usergroups.md)
* [Usergroups Users](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/usergroups-users.md)
* [Users](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/users.md)
* [Users Profile](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/users-profile.md)
* [Views](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/views.md)
* [Workflows](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/controllers/workflows.md)

## SDK Infrastructure

### Configuration

* [ProxySettings](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/proxy-settings.md)
* [Environment-Based Client Initialization](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/environment-based-client-initialization.md)
* [AbstractLogger](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/abstract-logger.md)
* [LoggingConfiguration](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/logging-configuration.md)
* [RequestLoggingConfiguration](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/request-logging-configuration.md)
* [ResponseLoggingConfiguration](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/response-logging-configuration.md)

### HTTP

* [HttpResponse](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/http-response.md)
* [HttpRequest](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/http-request.md)

### Utilities

* [ApiResponse](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/api-response.md)
* [ApiHelper](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/api-helper.md)
* [DateTimeHelper](https://www.github.com/sdks-io/slack-apimatic-sdk-ruby-sdk/tree/1.0.1/doc/date-time-helper.md)

