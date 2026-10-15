# postboost.AccountsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**connect_channel**](AccountsApi.md#connect_channel) | **POST** /{workspaceUuid}/accounts/connect/{provider} | Connect a Telegram, Discord or Slack channel
[**create_connect_link**](AccountsApi.md#create_connect_link) | **POST** /{workspaceUuid}/accounts/connect-links | Create a connect link
[**create_reconnect_link**](AccountsApi.md#create_reconnect_link) | **POST** /{workspaceUuid}/accounts/{accountUuid}/reconnect-links | Create a reconnect link
[**get_account**](AccountsApi.md#get_account) | **GET** /{workspaceUuid}/accounts/{accountUuid} | Get account
[**get_account_health**](AccountsApi.md#get_account_health) | **GET** /{workspaceUuid}/account-health | Account health
[**list_accounts**](AccountsApi.md#list_accounts) | **GET** /{workspaceUuid}/accounts | List accounts


# **connect_channel**
> ChannelAccount connect_channel(workspace_uuid, provider, connect_channel_input)

Connect a Telegram, Discord or Slack channel

Connects a channel that uses a bot token or a webhook URL instead of a login. The credentials are checked against the network first, stored encrypted and never returned. Connecting the same channel again updates it (`200`) instead of adding a second account. Workspace admins only; counts toward the plan's social account limit.  - **telegram**: `bot_token` from @BotFather and `chat` (the channel's `@username`, or its   numeric id such as `-1001234567890` for a private channel). The bot must be an administrator   of the channel allowed to post messages. - **discord**: `webhook_url` from Channel settings → Integrations → Webhooks   (`https://discord.com/api/webhooks/…`). - **slack**: `webhook_url` of an incoming webhook (`https://hooks.slack.com/services/…`) and an   optional display `name`. Slack posts cannot be deleted from PostBoost, and images must be   publicly reachable.  Webhook URLs on any other host are refused (`422`) before any request is made. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.channel_account import ChannelAccount
from postboost.models.connect_channel_input import ConnectChannelInput
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AccountsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    provider = 'provider_example' # str | 
    connect_channel_input = postboost.ConnectChannelInput() # ConnectChannelInput | 

    try:
        # Connect a Telegram, Discord or Slack channel
        api_response = api_instance.connect_channel(workspace_uuid, provider, connect_channel_input)
        print("The response of AccountsApi->connect_channel:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountsApi->connect_channel: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **provider** | **str**|  | 
 **connect_channel_input** | [**ConnectChannelInput**](ConnectChannelInput.md)|  | 

### Return type

[**ChannelAccount**](ChannelAccount.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Channel connected. |  -  |
**200** | The channel was already connected; its details and credentials were updated. |  -  |
**401** |  |  -  |
**403** | The caller is not a workspace admin, or the plan&#39;s social account limit is reached. |  -  |
**404** | Unknown provider, or the channel is switched off on this instance. |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_connect_link**
> ConnectLink create_connect_link(workspace_uuid, create_connect_link_request)

Create a connect link

Creates a single-use link (valid 15 minutes) to connect a new account on an OAuth network to this workspace: ask the user to open it in their browser while logged in to PostBoost, wait until they confirm, then call `list-accounts` to get the new account id. The link signs no one in: only the user who created it, while a workspace admin, can use it. Telegram, Discord and Slack need no browser: connect them with `connectChannel`. Mastodon, Pixelfed and Bluesky ask for a server or handle first, so the user connects them in the app. Workspace admins only; at most 10 links per minute. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.connect_link import ConnectLink
from postboost.models.create_connect_link_request import CreateConnectLinkRequest
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AccountsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    create_connect_link_request = postboost.CreateConnectLinkRequest() # CreateConnectLinkRequest | 

    try:
        # Create a connect link
        api_response = api_instance.create_connect_link(workspace_uuid, create_connect_link_request)
        print("The response of AccountsApi->create_connect_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountsApi->create_connect_link: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **create_connect_link_request** | [**CreateConnectLinkRequest**](CreateConnectLinkRequest.md)|  | 

### Return type

[**ConnectLink**](ConnectLink.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Link created. The URL is shown only once. |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |
**429** | Too many connect links in the last minute. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_reconnect_link**
> ReconnectLink create_reconnect_link(workspace_uuid, account_uuid)

Create a reconnect link

Creates a single-use link (valid 7 days) that lets someone without a PostBoost login, such as an agency's client, re-authorize this one account on its network. The link only refreshes the connection of this account; signing in as a different profile or page changes nothing. Workspace admins only. Available for Facebook Pages, Instagram, Threads, LinkedIn, TikTok, YouTube and Pinterest. Returns `404` while the feature is not enabled on this instance. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.reconnect_link import ReconnectLink
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AccountsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_uuid = 'account_uuid_example' # str | UUID of the social media account.

    try:
        # Create a reconnect link
        api_response = api_instance.create_reconnect_link(workspace_uuid, account_uuid)
        print("The response of AccountsApi->create_reconnect_link:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountsApi->create_reconnect_link: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_uuid** | **str**| UUID of the social media account. | 

### Return type

[**ReconnectLink**](ReconnectLink.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Link created. The URL is shown only once. |  -  |
**401** |  |  -  |
**403** | The caller is not a workspace admin, or not a member of the workspace. |  -  |
**404** | Unknown account, or reconnect links are not enabled. |  -  |
**422** | Reconnect links are not available for this account&#39;s network. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_account**
> Account get_account(workspace_uuid, account_uuid)

Get account

Returns a single social media account.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.account import Account
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AccountsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_uuid = 'account_uuid_example' # str | UUID of the social media account.

    try:
        # Get account
        api_response = api_instance.get_account(workspace_uuid, account_uuid)
        print("The response of AccountsApi->get_account:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountsApi->get_account: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_uuid** | **str**| UUID of the social media account. | 

### Return type

[**Account**](Account.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Account details |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_account_health**
> GetAccountHealth200Response get_account_health(workspace_uuid)

Account health

Pre-flight health of every account in the workspace: whether it is authorized and holds an access token, how much of its daily post cap (per UTC day, scheduled, awaiting approval and published posts) is used today, and its connection health: predicted token expiry, latest publish outcome and where to reconnect it. The `account.token_expiring` and `account.disconnected` webhooks report changes as they happen. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_account_health200_response import GetAccountHealth200Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AccountsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # Account health
        api_response = api_instance.get_account_health(workspace_uuid)
        print("The response of AccountsApi->get_account_health:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountsApi->get_account_health: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**GetAccountHealth200Response**](GetAccountHealth200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Health per account |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_accounts**
> ListAccounts200Response list_accounts(workspace_uuid, keyword=keyword, group=group, providers=providers, unauthorized=unauthorized)

List accounts

Returns all social media accounts connected to the workspace, newest first. Optional filters narrow the list.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_accounts200_response import ListAccounts200Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.AccountsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    keyword = 'keyword_example' # str | Match the account name or username. (optional)
    group = 'group_example' # str | Only accounts in this account group. (optional)
    providers = ['providers_example'] # List[str] | Only accounts of these providers (for example `instagram`, `linkedin`). (optional)
    unauthorized = True # bool | When `true`, only accounts that need to be reconnected. (optional)

    try:
        # List accounts
        api_response = api_instance.list_accounts(workspace_uuid, keyword=keyword, group=group, providers=providers, unauthorized=unauthorized)
        print("The response of AccountsApi->list_accounts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountsApi->list_accounts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **keyword** | **str**| Match the account name or username. | [optional] 
 **group** | **str**| Only accounts in this account group. | [optional] 
 **providers** | [**List[str]**](str.md)| Only accounts of these providers (for example &#x60;instagram&#x60;, &#x60;linkedin&#x60;). | [optional] 
 **unauthorized** | **bool**| When &#x60;true&#x60;, only accounts that need to be reconnected. | [optional] 

### Return type

[**ListAccounts200Response**](ListAccounts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of accounts |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

