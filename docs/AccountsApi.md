# postboost.AccountsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_account**](AccountsApi.md#get_account) | **GET** /{workspaceUuid}/accounts/{accountUuid} | Get account
[**list_accounts**](AccountsApi.md#list_accounts) | **GET** /{workspaceUuid}/accounts | List accounts


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

