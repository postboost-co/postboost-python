# postboost.PostingScheduleApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_posting_schedule**](PostingScheduleApi.md#get_posting_schedule) | **GET** /{workspaceUuid}/posting-schedule | Get the posting schedule
[**get_recommended_posting_times**](PostingScheduleApi.md#get_recommended_posting_times) | **GET** /{workspaceUuid}/posting-schedule/recommended | Get recommended posting times
[**list_queue_slots**](PostingScheduleApi.md#list_queue_slots) | **GET** /{workspaceUuid}/queue/slots | List upcoming queue slots
[**reset_account_posting_schedule**](PostingScheduleApi.md#reset_account_posting_schedule) | **DELETE** /{workspaceUuid}/posting-schedule/{accountId} | Reset an account schedule
[**update_posting_schedule**](PostingScheduleApi.md#update_posting_schedule) | **PUT** /{workspaceUuid}/posting-schedule | Set the posting schedule


# **get_posting_schedule**
> GetPostingSchedule200Response get_posting_schedule(workspace_uuid, account_id=account_id)

Get the posting schedule

The queue's posting times: per weekday, a list of clock times in the schedule's timezone. `account_id=0` is the workspace schedule. An account without its own schedule follows the workspace one (`inherited: true`, `source_account_id: 0`). Posts added to the queue take the next free time. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_posting_schedule200_response import GetPostingSchedule200Response
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
    api_instance = postboost.PostingScheduleApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_id = 0 # int | `0` (default) for the workspace schedule, or an account `id`. (optional) (default to 0)

    try:
        # Get the posting schedule
        api_response = api_instance.get_posting_schedule(workspace_uuid, account_id=account_id)
        print("The response of PostingScheduleApi->get_posting_schedule:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostingScheduleApi->get_posting_schedule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_id** | **int**| &#x60;0&#x60; (default) for the workspace schedule, or an account &#x60;id&#x60;. | [optional] [default to 0]

### Return type

[**GetPostingSchedule200Response**](GetPostingSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The schedule |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_recommended_posting_times**
> RecommendedPostingTimes get_recommended_posting_times(workspace_uuid, account_id=account_id, slots_per_day=slots_per_day)

Get recommended posting times

Suggested posting times from past engagement, in the schedule's timezone. `has_data` is false until there is enough analytics history. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.recommended_posting_times import RecommendedPostingTimes
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
    api_instance = postboost.PostingScheduleApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_id = 0 # int | `0` (default) for the workspace schedule, or an account `id`. (optional) (default to 0)
    slots_per_day = 56 # int | Times to suggest per day (1 to 6). (optional)

    try:
        # Get recommended posting times
        api_response = api_instance.get_recommended_posting_times(workspace_uuid, account_id=account_id, slots_per_day=slots_per_day)
        print("The response of PostingScheduleApi->get_recommended_posting_times:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostingScheduleApi->get_recommended_posting_times: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_id** | **int**| &#x60;0&#x60; (default) for the workspace schedule, or an account &#x60;id&#x60;. | [optional] [default to 0]
 **slots_per_day** | **int**| Times to suggest per day (1 to 6). | [optional] 

### Return type

[**RecommendedPostingTimes**](RecommendedPostingTimes.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Recommended times |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_queue_slots**
> QueueSlots list_queue_slots(workspace_uuid, account_id=account_id, after=after)

List upcoming queue slots

The queue read forward: upcoming posting times, filled by scheduled posts where they land on one. Page with `after` set to the previous `next_cursor`. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.queue_slots import QueueSlots
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
    api_instance = postboost.PostingScheduleApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_id = 0 # int | `0` (default) for the workspace schedule, or an account `id`. (optional) (default to 0)
    after = 'after_example' # str | Start after this time (`Y-m-d H:i:s`, UTC), from `next_cursor`. (optional)

    try:
        # List upcoming queue slots
        api_response = api_instance.list_queue_slots(workspace_uuid, account_id=account_id, after=after)
        print("The response of PostingScheduleApi->list_queue_slots:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostingScheduleApi->list_queue_slots: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_id** | **int**| &#x60;0&#x60; (default) for the workspace schedule, or an account &#x60;id&#x60;. | [optional] [default to 0]
 **after** | **str**| Start after this time (&#x60;Y-m-d H:i:s&#x60;, UTC), from &#x60;next_cursor&#x60;. | [optional] 

### Return type

[**QueueSlots**](QueueSlots.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Upcoming slots |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reset_account_posting_schedule**
> GetPostingSchedule200Response reset_account_posting_schedule(workspace_uuid, account_id)

Reset an account schedule

Removes the account's own schedule so it follows the workspace schedule again. Workspace admins only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_posting_schedule200_response import GetPostingSchedule200Response
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
    api_instance = postboost.PostingScheduleApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_id = 56 # int | The account `id`.

    try:
        # Reset an account schedule
        api_response = api_instance.reset_account_posting_schedule(workspace_uuid, account_id)
        print("The response of PostingScheduleApi->reset_account_posting_schedule:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostingScheduleApi->reset_account_posting_schedule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_id** | **int**| The account &#x60;id&#x60;. | 

### Return type

[**GetPostingSchedule200Response**](GetPostingSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The schedule now in effect for the account |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_posting_schedule**
> GetPostingSchedule200Response update_posting_schedule(workspace_uuid, posting_schedule_input)

Set the posting schedule

Sets the workspace schedule (`account_id: 0`) or gives one account its own schedule. Send all seven weekdays (ids 1 to 6 for Monday to Saturday, 0 for Sunday). Workspace admins only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_posting_schedule200_response import GetPostingSchedule200Response
from postboost.models.posting_schedule_input import PostingScheduleInput
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
    api_instance = postboost.PostingScheduleApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    posting_schedule_input = postboost.PostingScheduleInput() # PostingScheduleInput | 

    try:
        # Set the posting schedule
        api_response = api_instance.update_posting_schedule(workspace_uuid, posting_schedule_input)
        print("The response of PostingScheduleApi->update_posting_schedule:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostingScheduleApi->update_posting_schedule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **posting_schedule_input** | [**PostingScheduleInput**](PostingScheduleInput.md)|  | 

### Return type

[**GetPostingSchedule200Response**](GetPostingSchedule200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The schedule now in effect |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

