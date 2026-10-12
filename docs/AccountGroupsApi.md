# postboost.AccountGroupsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_account_group**](AccountGroupsApi.md#create_account_group) | **POST** /{workspaceUuid}/account-groups | Create an account group
[**delete_account_group**](AccountGroupsApi.md#delete_account_group) | **DELETE** /{workspaceUuid}/account-groups/{accountGroupUuid} | Delete an account group
[**get_account_group**](AccountGroupsApi.md#get_account_group) | **GET** /{workspaceUuid}/account-groups/{accountGroupUuid} | Get an account group
[**list_account_groups**](AccountGroupsApi.md#list_account_groups) | **GET** /{workspaceUuid}/account-groups | List account groups
[**update_account_group**](AccountGroupsApi.md#update_account_group) | **PUT** /{workspaceUuid}/account-groups/{accountGroupUuid} | Update an account group


# **create_account_group**
> CreateAccountGroup201Response create_account_group(workspace_uuid, account_group_input)

Create an account group

Creates a named set of accounts of this workspace. Admins and members only (not viewers). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.account_group_input import AccountGroupInput
from postboost.models.create_account_group201_response import CreateAccountGroup201Response
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
    api_instance = postboost.AccountGroupsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_group_input = postboost.AccountGroupInput() # AccountGroupInput | 

    try:
        # Create an account group
        api_response = api_instance.create_account_group(workspace_uuid, account_group_input)
        print("The response of AccountGroupsApi->create_account_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountGroupsApi->create_account_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_group_input** | [**AccountGroupInput**](AccountGroupInput.md)|  | 

### Return type

[**CreateAccountGroup201Response**](CreateAccountGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The new account group |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_account_group**
> delete_account_group(workspace_uuid, account_group_uuid)

Delete an account group

Deletes the group, not its accounts. Admins and members only (not viewers). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
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
    api_instance = postboost.AccountGroupsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_group_uuid = 'account_group_uuid_example' # str | The account group `uuid`.

    try:
        # Delete an account group
        api_instance.delete_account_group(workspace_uuid, account_group_uuid)
    except Exception as e:
        print("Exception when calling AccountGroupsApi->delete_account_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_group_uuid** | **str**| The account group &#x60;uuid&#x60;. | 

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Deleted |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_account_group**
> CreateAccountGroup201Response get_account_group(workspace_uuid, account_group_uuid)

Get an account group

One account group. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_account_group201_response import CreateAccountGroup201Response
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
    api_instance = postboost.AccountGroupsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_group_uuid = 'account_group_uuid_example' # str | The account group `uuid`.

    try:
        # Get an account group
        api_response = api_instance.get_account_group(workspace_uuid, account_group_uuid)
        print("The response of AccountGroupsApi->get_account_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountGroupsApi->get_account_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_group_uuid** | **str**| The account group &#x60;uuid&#x60;. | 

### Return type

[**CreateAccountGroup201Response**](CreateAccountGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The account group |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_account_groups**
> ListAccountGroups200Response list_account_groups(workspace_uuid, page=page, per_page=per_page)

List account groups

Named sets of accounts, sorted by name, with their account ids. Pass `account_ids` as `accounts` when you create a post to publish to the whole group. Paginated with `page` and `per_page` (default 100). A key limited to some accounts only sees groups whose accounts are all among its accounts, and `meta.total` counts only those. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_account_groups200_response import ListAccountGroups200Response
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
    api_instance = postboost.AccountGroupsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    page = 1 # int | Page number (1-based). (optional) (default to 1)
    per_page = 100 # int | Items per page, 1-100. (optional) (default to 100)

    try:
        # List account groups
        api_response = api_instance.list_account_groups(workspace_uuid, page=page, per_page=per_page)
        print("The response of AccountGroupsApi->list_account_groups:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountGroupsApi->list_account_groups: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **page** | **int**| Page number (1-based). | [optional] [default to 1]
 **per_page** | **int**| Items per page, 1-100. | [optional] [default to 100]

### Return type

[**ListAccountGroups200Response**](ListAccountGroups200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Account groups, paginated (&#x60;links&#x60; and &#x60;meta&#x60; as on the other list endpoints) |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_account_group**
> CreateAccountGroup201Response update_account_group(workspace_uuid, account_group_uuid, account_group_input)

Update an account group

Replaces the name and the accounts of the group (accounts you leave out are removed). Admins and members only (not viewers). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.account_group_input import AccountGroupInput
from postboost.models.create_account_group201_response import CreateAccountGroup201Response
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
    api_instance = postboost.AccountGroupsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_group_uuid = 'account_group_uuid_example' # str | The account group `uuid`.
    account_group_input = postboost.AccountGroupInput() # AccountGroupInput | 

    try:
        # Update an account group
        api_response = api_instance.update_account_group(workspace_uuid, account_group_uuid, account_group_input)
        print("The response of AccountGroupsApi->update_account_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountGroupsApi->update_account_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_group_uuid** | **str**| The account group &#x60;uuid&#x60;. | 
 **account_group_input** | [**AccountGroupInput**](AccountGroupInput.md)|  | 

### Return type

[**CreateAccountGroup201Response**](CreateAccountGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated account group |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

