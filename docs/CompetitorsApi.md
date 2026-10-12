# postboost.CompetitorsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_competitor**](CompetitorsApi.md#add_competitor) | **POST** /{workspaceUuid}/competitors | Track a competitor
[**delete_competitor**](CompetitorsApi.md#delete_competitor) | **DELETE** /{workspaceUuid}/competitors/{competitorId} | Stop tracking a competitor
[**get_competitor**](CompetitorsApi.md#get_competitor) | **GET** /{workspaceUuid}/competitors/{competitorId} | Get a competitor
[**list_competitors**](CompetitorsApi.md#list_competitors) | **GET** /{workspaceUuid}/competitors | List competitors


# **add_competitor**
> AddCompetitor202Response add_competitor(workspace_uuid, competitor_input)

Track a competitor

Starts tracking a public Instagram business or creator account from one of your Instagram accounts (connected through a Facebook Page). Returns `202` at once; followers, snapshots and recent media appear after the background import. `409` if that account already tracks the username. Admins and members only (not viewers). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.add_competitor202_response import AddCompetitor202Response
from postboost.models.competitor_input import CompetitorInput
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
    api_instance = postboost.CompetitorsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    competitor_input = postboost.CompetitorInput() # CompetitorInput | 

    try:
        # Track a competitor
        api_response = api_instance.add_competitor(workspace_uuid, competitor_input)
        print("The response of CompetitorsApi->add_competitor:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompetitorsApi->add_competitor: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **competitor_input** | [**CompetitorInput**](CompetitorInput.md)|  | 

### Return type

[**AddCompetitor202Response**](AddCompetitor202Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Tracking started; the import runs in the background |  -  |
**409** | Already tracked |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_competitor**
> delete_competitor(workspace_uuid, competitor_id)

Stop tracking a competitor

Deletes the competitor with its snapshots and media. Admins and members only (not viewers). 

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
    api_instance = postboost.CompetitorsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    competitor_id = 56 # int | The competitor `id`.

    try:
        # Stop tracking a competitor
        api_instance.delete_competitor(workspace_uuid, competitor_id)
    except Exception as e:
        print("Exception when calling CompetitorsApi->delete_competitor: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **competitor_id** | **int**| The competitor &#x60;id&#x60;. | 

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

# **get_competitor**
> GetCompetitor200Response get_competitor(workspace_uuid, competitor_id)

Get a competitor

The competitor with daily follower snapshots for the last 90 days and its 12 most recent posts. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_competitor200_response import GetCompetitor200Response
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
    api_instance = postboost.CompetitorsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    competitor_id = 56 # int | The competitor `id`.

    try:
        # Get a competitor
        api_response = api_instance.get_competitor(workspace_uuid, competitor_id)
        print("The response of CompetitorsApi->get_competitor:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompetitorsApi->get_competitor: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **competitor_id** | **int**| The competitor &#x60;id&#x60;. | 

### Return type

[**GetCompetitor200Response**](GetCompetitor200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The competitor |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_competitors**
> ListCompetitors200Response list_competitors(workspace_uuid, account_id=account_id)

List competitors

Instagram business or creator accounts the workspace tracks, by follower count. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_competitors200_response import ListCompetitors200Response
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
    api_instance = postboost.CompetitorsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_id = 56 # int | Only competitors tracked from this Instagram account `id`. (optional)

    try:
        # List competitors
        api_response = api_instance.list_competitors(workspace_uuid, account_id=account_id)
        print("The response of CompetitorsApi->list_competitors:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompetitorsApi->list_competitors: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_id** | **int**| Only competitors tracked from this Instagram account &#x60;id&#x60;. | [optional] 

### Return type

[**ListCompetitors200Response**](ListCompetitors200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Competitors |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

