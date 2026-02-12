
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](../README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| connection | `Faraday::Connection` | The Faraday connection object passed by the SDK user for making requests |
| adapter | `Faraday::Adapter` | The Faraday adapter object passed by the SDK user for performing http requests |
| timeout | `Float` | The value to use for connection timeout. <br> **Default: 30** |
| max_retries | `Integer` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| retry_interval | `Float` | Pause in seconds between retries. <br> **Default: 1** |
| backoff_factor | `Float` | The amount to multiply each successive retry's interval amount by in order to provide backoff. <br> **Default: 2** |
| retry_statuses | `Array` | A list of HTTP statuses to retry. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array` | A list of HTTP methods to retry. <br> **Default: %i[get put]** |
| http_callback | `HttpCallBack` | The Http CallBack allows defining callables for pre and post API calls. |
| proxy_settings | [`ProxySettings`](../doc/proxy-settings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](../doc/logging-configuration.md) | The SDK logging configuration for API calls |
| authorization_code_auth_credentials | [`AuthorizationCodeAuthCredentials`](auth/oauth-2-authorization-code-grant.md) | The credential object for OAuth 2 Authorization Code Grant |

The API client can be initialized as follows:

## Code-Based Client Initialization

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

## Environment-Based Client Initialization

```ruby
require 'slack_web_api'
include SlackWebApi

# Create client from environment
client = Client.from_env
```

See the [`Environment-Based Client Initialization`](../doc/environment-based-client-initialization.md) section for details.

## Slack Web API Client

The gateway for the SDK. This class acts as a factory for the Apis and also holds the configuration of the SDK.

## Apis

| Name | Description |
|  --- | --- |
| admin_apps | Gets AdminAppsApi |
| admin_apps_approved | Gets AdminAppsApprovedApi |
| admin_apps_requests | Gets AdminAppsRequestsApi |
| admin_apps_restricted | Gets AdminAppsRestrictedApi |
| admin_conversations | Gets AdminConversationsApi |
| admin_conversations_ekm | Gets AdminConversationsEkmApi |
| admin_conversations_restrict_access | Gets AdminConversationsRestrictAccessApi |
| admin_emoji | Gets AdminEmojiApi |
| admin_invite_requests | Gets AdminInviteRequestsApi |
| admin_invite_requests_approved | Gets AdminInviteRequestsApprovedApi |
| admin_invite_requests_denied | Gets AdminInviteRequestsDeniedApi |
| admin_teams_admins | Gets AdminTeamsAdminsApi |
| admin_teams | Gets AdminTeamsApi |
| admin_teams_owners | Gets AdminTeamsOwnersApi |
| admin_teams_settings | Gets AdminTeamsSettingsApi |
| admin_usergroups | Gets AdminUsergroupsApi |
| admin_users | Gets AdminUsersApi |
| admin_users_session | Gets AdminUsersSessionApi |
| api | Gets Api |
| apps_event_authorizations | Gets AppsEventAuthorizationsApi |
| apps_permissions | Gets AppsPermissionsApi |
| apps_permissions_resources | Gets AppsPermissionsResourcesApi |
| apps_permissions_scopes | Gets AppsPermissionsScopesApi |
| apps_permissions_users | Gets AppsPermissionsUsersApi |
| apps | Gets AppsApi |
| auth | Gets AuthApi |
| bots | Gets BotsApi |
| calls | Gets CallsApi |
| calls_participants | Gets CallsParticipantsApi |
| chat | Gets ChatApi |
| chat_scheduled_messages | Gets ChatScheduledMessagesApi |
| conversations | Gets ConversationsApi |
| dialog | Gets DialogApi |
| dnd | Gets DndApi |
| emoji | Gets EmojiApi |
| files_comments | Gets FilesCommentsApi |
| files | Gets FilesApi |
| files_remote | Gets FilesRemoteApi |
| migration | Gets MigrationApi |
| oauth | Gets OauthApi |
| oauth_v_2 | Gets OauthV2Api |
| pins | Gets PinsApi |
| reactions | Gets ReactionsApi |
| reminders | Gets RemindersApi |
| rtm | Gets RtmApi |
| search | Gets SearchApi |
| stars | Gets StarsApi |
| team | Gets TeamApi |
| team_profile | Gets TeamProfileApi |
| usergroups | Gets UsergroupsApi |
| usergroups_users | Gets UsergroupsUsersApi |
| users | Gets UsersApi |
| users_profile | Gets UsersProfileApi |
| views | Gets ViewsApi |
| workflows | Gets WorkflowsApi |
| oauth_authorization | Gets OauthAuthorizationApi |

