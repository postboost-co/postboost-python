# postboost.ActivityApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_api_activity**](ActivityApi.md#list_api_activity) | **GET** /{workspaceUuid}/activity | List API activity


# **list_api_activity**
> ListApiActivity200Response list_api_activity(workspace_uuid, outcome=outcome, client=client, since=since, page=page)

List API activity

Every write request (`POST`, `PUT`, `DELETE`) made through the API in this workspace, newest first, with the client that made it and its outcome. Kept for 90 days. Send an `X-PostBoost-Client` header (for example `my-agent/1.2`) to label your requests; otherwise the `User-Agent` is recorded. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.api_activity_outcome import ApiActivityOutcome
from postboost.models.list_api_activity200_response import ListApiActivity200Response
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
    api_instance = postboost.ActivityApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    outcome = postboost.ApiActivityOutcome() # ApiActivityOutcome |  (optional)
    client = 'client_example' # str | Client label prefix, for example `mcp`. (optional)
    since = '2013-10-20T19:20:30+01:00' # datetime | Only entries at or after this time (UTC). (optional)
    page = 1 # int |  (optional) (default to 1)

    try:
        # List API activity
        api_response = api_instance.list_api_activity(workspace_uuid, outcome=outcome, client=client, since=since, page=page)
        print("The response of ActivityApi->list_api_activity:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ActivityApi->list_api_activity: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **outcome** | [**ApiActivityOutcome**](.md)|  | [optional] 
 **client** | **str**| Client label prefix, for example &#x60;mcp&#x60;. | [optional] 
 **since** | **datetime**| Only entries at or after this time (UTC). | [optional] 
 **page** | **int**|  | [optional] [default to 1]

### Return type

[**ListApiActivity200Response**](ListApiActivity200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated activity entries (50 per page) |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

