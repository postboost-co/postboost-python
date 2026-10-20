# postboost.WorkspacesApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_user_to_workspace**](WorkspacesApi.md#add_user_to_workspace) | **POST** /panel/workspaces/{workspaceUuid}/users | Add user to workspace
[**create_api_key**](WorkspacesApi.md#create_api_key) | **POST** /{workspaceUuid}/api-keys | Create a scoped API key
[**create_reseller_client**](WorkspacesApi.md#create_reseller_client) | **POST** /{workspaceUuid}/clients | Create a client workspace
[**create_workspace**](WorkspacesApi.md#create_workspace) | **POST** /panel/workspaces | Create workspace
[**delete_api_key**](WorkspacesApi.md#delete_api_key) | **DELETE** /{workspaceUuid}/api-keys/{apiKeyId} | Revoke a scoped API key
[**delete_workspace**](WorkspacesApi.md#delete_workspace) | **DELETE** /panel/workspaces/{workspaceUuid} | Delete workspace
[**delete_workspaces_bulk**](WorkspacesApi.md#delete_workspaces_bulk) | **DELETE** /panel/workspaces | Delete workspaces (bulk)
[**get_workspace**](WorkspacesApi.md#get_workspace) | **GET** /panel/workspaces/{workspaceUuid} | Get workspace
[**get_workspace_ai_credits**](WorkspacesApi.md#get_workspace_ai_credits) | **GET** /panel/workspaces/{workspaceUuid}/ai-credits | Get workspace AI credits
[**get_x_usage**](WorkspacesApi.md#get_x_usage) | **GET** /{workspaceUuid}/usage/x | X (Twitter) usage
[**list_api_keys**](WorkspacesApi.md#list_api_keys) | **GET** /{workspaceUuid}/api-keys | List scoped API keys
[**list_my_workspaces**](WorkspacesApi.md#list_my_workspaces) | **GET** /workspaces | List my workspaces
[**list_reseller_clients**](WorkspacesApi.md#list_reseller_clients) | **GET** /{workspaceUuid}/clients | List client workspaces
[**list_workspaces**](WorkspacesApi.md#list_workspaces) | **GET** /panel/workspaces | List workspaces
[**remove_user_from_workspace**](WorkspacesApi.md#remove_user_from_workspace) | **DELETE** /panel/workspaces/{workspaceUuid}/users | Remove user from workspace
[**update_workspace**](WorkspacesApi.md#update_workspace) | **PUT** /panel/workspaces/{workspaceUuid} | Update workspace
[**update_workspace_user**](WorkspacesApi.md#update_workspace_user) | **PUT** /panel/workspaces/{workspaceUuid}/users | Update user role in workspace


# **add_user_to_workspace**
> object add_user_to_workspace(workspace_uuid, workspace_user_input)

Add user to workspace

Adds an existing user to the workspace with a specified role. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.workspace_user_input import WorkspaceUserInput
from postboost.models.object import object
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    workspace_user_input = postboost.WorkspaceUserInput() # WorkspaceUserInput | 

    try:
        # Add user to workspace
        api_response = api_instance.add_user_to_workspace(workspace_uuid, workspace_user_input)
        print("The response of WorkspacesApi->add_user_to_workspace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->add_user_to_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **workspace_user_input** | [**WorkspaceUserInput**](WorkspaceUserInput.md)|  | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_api_key**
> CreateApiKey201Response create_api_key(workspace_uuid, api_key_input)

Create a scoped API key

Creates a least-privilege API key for the calling user, bound to this workspace. Pick the abilities it gets and, optionally, the accounts it may act on. The plain key is in `data.token` of this response only; store it safely.  | Ability | Allows | |---|---| | `read` | Every `GET`, plus the `posts/validate` dry run | | `write` | Creating and changing drafts, media, tags, mentions, the brand voice | | `publish` | Scheduling, queueing, publishing now, approving and retrying posts, and editing a post that is already scheduled | | `ai` | The `/ai/*` endpoints, running agents and turning on agent AI review (they also need AI credits) | | `webhooks` | Webhook subscription endpoints |  A scoped key is refused on other workspaces, on the admin panel, on API key management and on the app's built-in MCP endpoint (use `/mcp/postboost`). With `account_ids`, it may only name those accounts (in the URL, `accounts`, `account_ids` or post versions), cannot touch posts on other accounts, and `GET accounts` / `GET posts` only list matching items (pagination counts are computed before that filter). Workspace admins only, called with an unscoped key. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.api_key_input import ApiKeyInput
from postboost.models.create_api_key201_response import CreateApiKey201Response
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    api_key_input = {"name":"Reporting agent","abilities":["read"],"account_ids":[12,14],"expires_at":"2027-01-31"} # ApiKeyInput | 

    try:
        # Create a scoped API key
        api_response = api_instance.create_api_key(workspace_uuid, api_key_input)
        print("The response of WorkspacesApi->create_api_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->create_api_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **api_key_input** | [**ApiKeyInput**](ApiKeyInput.md)|  | 

### Return type

[**CreateApiKey201Response**](CreateApiKey201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The new key, with its plain token shown once |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_reseller_client**
> CreateResellerClient201Response create_reseller_client(workspace_uuid, reseller_client_input)

Create a client workspace

Creates a client workspace on the Reseller client plan, with the caller as its owner and admin, and links it to this workspace. Fails with `422` and `code: client_limit_reached` once the plan's client limit is used (archived clients do not count). Archive clients on the Client workspaces page. Workspace admins with an unscoped key only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_reseller_client201_response import CreateResellerClient201Response
from postboost.models.reseller_client_input import ResellerClientInput
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    reseller_client_input = {"name":"Acme Bakery"} # ResellerClientInput | 

    try:
        # Create a client workspace
        api_response = api_instance.create_reseller_client(workspace_uuid, reseller_client_input)
        print("The response of WorkspacesApi->create_reseller_client:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->create_reseller_client: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **reseller_client_input** | [**ResellerClientInput**](ResellerClientInput.md)|  | 

### Return type

[**CreateResellerClient201Response**](CreateResellerClient201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The client workspace was created |  -  |
**401** |  |  -  |
**403** | Not a workspace admin, a scoped key, or the workspace is not on the Reseller plan (&#x60;code: not_a_reseller&#x60;) |  -  |
**422** | Validation error or client limit reached (&#x60;code: client_limit_reached&#x60;) |  -  |
**503** | Client workspaces are not set up yet (&#x60;code: client_plan_missing&#x60;) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_workspace**
> Workspace create_workspace(workspace_input)

Create workspace

Create a new workspace. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.workspace import Workspace
from postboost.models.workspace_input import WorkspaceInput
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_input = postboost.WorkspaceInput() # WorkspaceInput | 

    try:
        # Create workspace
        api_response = api_instance.create_workspace(workspace_input)
        print("The response of WorkspacesApi->create_workspace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->create_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_input** | [**WorkspaceInput**](WorkspaceInput.md)|  | 

### Return type

[**Workspace**](Workspace.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created workspace |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_api_key**
> object delete_api_key(workspace_uuid, api_key_id)

Revoke a scoped API key

Revokes a scoped key bound to this workspace. It stops working at once. Workspace admins only, called with an unscoped key.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.object import object
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    api_key_id = 56 # int | The key's `id` from `GET api-keys`.

    try:
        # Revoke a scoped API key
        api_response = api_instance.delete_api_key(workspace_uuid, api_key_id)
        print("The response of WorkspacesApi->delete_api_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->delete_api_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **api_key_id** | **int**| The key&#39;s &#x60;id&#x60; from &#x60;GET api-keys&#x60;. | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_workspace**
> object delete_workspace(workspace_uuid)

Delete workspace

Permanently deletes a single workspace and all its associated data. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.object import object
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # Delete workspace
        api_response = api_instance.delete_workspace(workspace_uuid)
        print("The response of WorkspacesApi->delete_workspace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->delete_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_workspaces_bulk**
> object delete_workspaces_bulk(delete_workspaces_bulk_request)

Delete workspaces (bulk)

Permanently deletes one or more workspaces and all their associated data. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.delete_workspaces_bulk_request import DeleteWorkspacesBulkRequest
from postboost.models.object import object
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
    api_instance = postboost.WorkspacesApi(api_client)
    delete_workspaces_bulk_request = postboost.DeleteWorkspacesBulkRequest() # DeleteWorkspacesBulkRequest | 

    try:
        # Delete workspaces (bulk)
        api_response = api_instance.delete_workspaces_bulk(delete_workspaces_bulk_request)
        print("The response of WorkspacesApi->delete_workspaces_bulk:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->delete_workspaces_bulk: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delete_workspaces_bulk_request** | [**DeleteWorkspacesBulkRequest**](DeleteWorkspacesBulkRequest.md)|  | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_workspace**
> Workspace get_workspace(workspace_uuid)

Get workspace

Returns a single workspace by UUID including its subscription status. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.workspace import Workspace
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # Get workspace
        api_response = api_instance.get_workspace(workspace_uuid)
        print("The response of WorkspacesApi->get_workspace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**Workspace**](Workspace.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Workspace details |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_workspace_ai_credits**
> AICredits get_workspace_ai_credits(workspace_uuid)

Get workspace AI credits

Returns whether the workspace can use AI credits, its remaining balance, and whether the balance is low. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.ai_credits import AICredits
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # Get workspace AI credits
        api_response = api_instance.get_workspace_ai_credits(workspace_uuid)
        print("The response of WorkspacesApi->get_workspace_ai_credits:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_workspace_ai_credits: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**AICredits**](AICredits.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | AI credit status |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_x_usage**
> XUsage get_x_usage(workspace_uuid)

X (Twitter) usage

The workspace's X posts this calendar month (UTC) against its monthly X allowance. Every thread part is one X post; a part with a link also counts as a link post. Once enforcement is switched on (`enforced: true`), scheduling to X is refused when the allowance is used up (`429`, `code: x_monthly_cap_reached`) and X posts that come due fail with \"Monthly X allowance reached\". Until then usage is tracked only. Other networks are not affected. See the X policy in the developer docs. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.x_usage import XUsage
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # X (Twitter) usage
        api_response = api_instance.get_x_usage(workspace_uuid)
        print("The response of WorkspacesApi->get_x_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->get_x_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**XUsage**](XUsage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Usage this month |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_api_keys**
> ListApiKeys200Response list_api_keys(workspace_uuid)

List scoped API keys

Scoped API keys bound to this workspace, newest first. The secret is never shown again after creation. Workspace admins only, called with an unscoped key (a scoped key gets `403` with `code: insufficient_scope`). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_api_keys200_response import ListApiKeys200Response
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # List scoped API keys
        api_response = api_instance.list_api_keys(workspace_uuid)
        print("The response of WorkspacesApi->list_api_keys:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->list_api_keys: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**ListApiKeys200Response**](ListApiKeys200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Scoped keys of this workspace |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_my_workspaces**
> ListMyWorkspaces200Response list_my_workspaces()

List my workspaces

Returns the workspaces the authenticated user belongs to, most recently updated first, with the caller's role in each. Use a returned `uuid` as `workspaceUuid`.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_my_workspaces200_response import ListMyWorkspaces200Response
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
    api_instance = postboost.WorkspacesApi(api_client)

    try:
        # List my workspaces
        api_response = api_instance.list_my_workspaces()
        print("The response of WorkspacesApi->list_my_workspaces:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->list_my_workspaces: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ListMyWorkspaces200Response**](ListMyWorkspaces200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The caller&#39;s workspaces |  -  |
**401** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_reseller_clients**
> ListResellerClients200Response list_reseller_clients(workspace_uuid)

List client workspaces

Client workspaces this workspace created on the Reseller plan, active first, then archived. `accounts_needing_reconnect` counts accounts whose connection must be renewed. `meta` gives the active clients and the plan's client limit. Workspace admins with an unscoped key only; other workspaces get `403` with `code: not_a_reseller`. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_reseller_clients200_response import ListResellerClients200Response
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # List client workspaces
        api_response = api_instance.list_reseller_clients(workspace_uuid)
        print("The response of WorkspacesApi->list_reseller_clients:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->list_reseller_clients: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**ListResellerClients200Response**](ListResellerClients200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The reseller&#39;s client workspaces |  -  |
**401** |  |  -  |
**403** | Not a workspace admin, a scoped key, or the workspace is not on the Reseller plan (&#x60;code: not_a_reseller&#x60;) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_workspaces**
> ListWorkspaces200Response list_workspaces(keyword=keyword, subscription_status=subscription_status, access_status=access_status, page=page)

List workspaces

Returns a paginated list of all workspaces. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_workspaces200_response import ListWorkspaces200Response
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
    api_instance = postboost.WorkspacesApi(api_client)
    keyword = 'keyword_example' # str |  (optional)
    subscription_status = 'subscription_status_example' # str |  (optional)
    access_status = 'access_status_example' # str |  (optional)
    page = 1 # int | Page number (15 items per page). (optional) (default to 1)

    try:
        # List workspaces
        api_response = api_instance.list_workspaces(keyword=keyword, subscription_status=subscription_status, access_status=access_status, page=page)
        print("The response of WorkspacesApi->list_workspaces:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->list_workspaces: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **keyword** | **str**|  | [optional] 
 **subscription_status** | **str**|  | [optional] 
 **access_status** | **str**|  | [optional] 
 **page** | **int**| Page number (15 items per page). | [optional] [default to 1]

### Return type

[**ListWorkspaces200Response**](ListWorkspaces200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated list of workspaces |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_user_from_workspace**
> object remove_user_from_workspace(workspace_uuid, remove_user_from_workspace_request)

Remove user from workspace

Removes a user's access to the workspace. The user account is not deleted. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.remove_user_from_workspace_request import RemoveUserFromWorkspaceRequest
from postboost.models.object import object
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    remove_user_from_workspace_request = postboost.RemoveUserFromWorkspaceRequest() # RemoveUserFromWorkspaceRequest | 

    try:
        # Remove user from workspace
        api_response = api_instance.remove_user_from_workspace(workspace_uuid, remove_user_from_workspace_request)
        print("The response of WorkspacesApi->remove_user_from_workspace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->remove_user_from_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **remove_user_from_workspace_request** | [**RemoveUserFromWorkspaceRequest**](RemoveUserFromWorkspaceRequest.md)|  | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_workspace**
> object update_workspace(workspace_uuid, workspace_input)

Update workspace

Updates a workspace's name, owner, or access status. Admin only. `hex_color` is accepted but ignored.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.workspace_input import WorkspaceInput
from postboost.models.object import object
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    workspace_input = postboost.WorkspaceInput() # WorkspaceInput | 

    try:
        # Update workspace
        api_response = api_instance.update_workspace(workspace_uuid, workspace_input)
        print("The response of WorkspacesApi->update_workspace:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->update_workspace: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **workspace_input** | [**WorkspaceInput**](WorkspaceInput.md)|  | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_workspace_user**
> object update_workspace_user(workspace_uuid, workspace_user_input)

Update user role in workspace

Changes a user's role or permissions within the workspace. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.workspace_user_input import WorkspaceUserInput
from postboost.models.object import object
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
    api_instance = postboost.WorkspacesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    workspace_user_input = postboost.WorkspaceUserInput() # WorkspaceUserInput | 

    try:
        # Update user role in workspace
        api_response = api_instance.update_workspace_user(workspace_uuid, workspace_user_input)
        print("The response of WorkspacesApi->update_workspace_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkspacesApi->update_workspace_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **workspace_user_input** | [**WorkspaceUserInput**](WorkspaceUserInput.md)|  | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

