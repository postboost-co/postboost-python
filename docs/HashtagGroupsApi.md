# postboost.HashtagGroupsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_hashtag_group**](HashtagGroupsApi.md#create_hashtag_group) | **POST** /{workspaceUuid}/hashtag-groups | Create a hashtag group
[**delete_hashtag_group**](HashtagGroupsApi.md#delete_hashtag_group) | **DELETE** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Delete a hashtag group
[**get_hashtag_group**](HashtagGroupsApi.md#get_hashtag_group) | **GET** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Get a hashtag group
[**list_hashtag_groups**](HashtagGroupsApi.md#list_hashtag_groups) | **GET** /{workspaceUuid}/hashtag-groups | List hashtag groups
[**update_hashtag_group**](HashtagGroupsApi.md#update_hashtag_group) | **PUT** /{workspaceUuid}/hashtag-groups/{hashtagGroupId} | Update a hashtag group


# **create_hashtag_group**
> CreateHashtagGroup201Response create_hashtag_group(workspace_uuid, hashtag_group_input)

Create a hashtag group

Saves a named set of hashtags (up to 3000 characters). Admins and members only (not viewers). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_hashtag_group201_response import CreateHashtagGroup201Response
from postboost.models.hashtag_group_input import HashtagGroupInput
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
    api_instance = postboost.HashtagGroupsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    hashtag_group_input = postboost.HashtagGroupInput() # HashtagGroupInput | 

    try:
        # Create a hashtag group
        api_response = api_instance.create_hashtag_group(workspace_uuid, hashtag_group_input)
        print("The response of HashtagGroupsApi->create_hashtag_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HashtagGroupsApi->create_hashtag_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **hashtag_group_input** | [**HashtagGroupInput**](HashtagGroupInput.md)|  | 

### Return type

[**CreateHashtagGroup201Response**](CreateHashtagGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The new hashtag group |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_hashtag_group**
> delete_hashtag_group(workspace_uuid, hashtag_group_id)

Delete a hashtag group

Admins and members only (not viewers). 

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
    api_instance = postboost.HashtagGroupsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    hashtag_group_id = 'hashtag_group_id_example' # str | The hashtag group `id`.

    try:
        # Delete a hashtag group
        api_instance.delete_hashtag_group(workspace_uuid, hashtag_group_id)
    except Exception as e:
        print("Exception when calling HashtagGroupsApi->delete_hashtag_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **hashtag_group_id** | **str**| The hashtag group &#x60;id&#x60;. | 

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

# **get_hashtag_group**
> CreateHashtagGroup201Response get_hashtag_group(workspace_uuid, hashtag_group_id)

Get a hashtag group

One hashtag group. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_hashtag_group201_response import CreateHashtagGroup201Response
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
    api_instance = postboost.HashtagGroupsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    hashtag_group_id = 'hashtag_group_id_example' # str | The hashtag group `id`.

    try:
        # Get a hashtag group
        api_response = api_instance.get_hashtag_group(workspace_uuid, hashtag_group_id)
        print("The response of HashtagGroupsApi->get_hashtag_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HashtagGroupsApi->get_hashtag_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **hashtag_group_id** | **str**| The hashtag group &#x60;id&#x60;. | 

### Return type

[**CreateHashtagGroup201Response**](CreateHashtagGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The hashtag group |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_hashtag_groups**
> ListHashtagGroups200Response list_hashtag_groups(workspace_uuid, page=page, per_page=per_page)

List hashtag groups

Saved hashtag sets of the workspace, newest first. Paginated with `page` and `per_page` (default 100). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_hashtag_groups200_response import ListHashtagGroups200Response
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
    api_instance = postboost.HashtagGroupsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    page = 1 # int | Page number (1-based). (optional) (default to 1)
    per_page = 100 # int | Items per page, 1-100. (optional) (default to 100)

    try:
        # List hashtag groups
        api_response = api_instance.list_hashtag_groups(workspace_uuid, page=page, per_page=per_page)
        print("The response of HashtagGroupsApi->list_hashtag_groups:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HashtagGroupsApi->list_hashtag_groups: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **page** | **int**| Page number (1-based). | [optional] [default to 1]
 **per_page** | **int**| Items per page, 1-100. | [optional] [default to 100]

### Return type

[**ListHashtagGroups200Response**](ListHashtagGroups200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Hashtag groups, paginated (&#x60;links&#x60; and &#x60;meta&#x60; as on the other list endpoints) |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_hashtag_group**
> CreateHashtagGroup201Response update_hashtag_group(workspace_uuid, hashtag_group_id, hashtag_group_input)

Update a hashtag group

Admins and members only (not viewers). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_hashtag_group201_response import CreateHashtagGroup201Response
from postboost.models.hashtag_group_input import HashtagGroupInput
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
    api_instance = postboost.HashtagGroupsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    hashtag_group_id = 'hashtag_group_id_example' # str | The hashtag group `id`.
    hashtag_group_input = postboost.HashtagGroupInput() # HashtagGroupInput | 

    try:
        # Update a hashtag group
        api_response = api_instance.update_hashtag_group(workspace_uuid, hashtag_group_id, hashtag_group_input)
        print("The response of HashtagGroupsApi->update_hashtag_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling HashtagGroupsApi->update_hashtag_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **hashtag_group_id** | **str**| The hashtag group &#x60;id&#x60;. | 
 **hashtag_group_input** | [**HashtagGroupInput**](HashtagGroupInput.md)|  | 

### Return type

[**CreateHashtagGroup201Response**](CreateHashtagGroup201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated hashtag group |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

