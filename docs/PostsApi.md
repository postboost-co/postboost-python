# postboost.PostsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_post_to_queue**](PostsApi.md#add_post_to_queue) | **POST** /{workspaceUuid}/posts/add-to-queue/{postUuid} | Add post to queue
[**approve_post**](PostsApi.md#approve_post) | **POST** /{workspaceUuid}/posts/approve/{postUuid} | Approve post
[**create_post**](PostsApi.md#create_post) | **POST** /{workspaceUuid}/posts | Create post
[**delete_post**](PostsApi.md#delete_post) | **DELETE** /{workspaceUuid}/posts/{postUuid} | Delete post
[**delete_posts_bulk**](PostsApi.md#delete_posts_bulk) | **DELETE** /{workspaceUuid}/posts | Delete posts (bulk)
[**get_post**](PostsApi.md#get_post) | **GET** /{workspaceUuid}/posts/{postUuid} | Get post
[**list_posts**](PostsApi.md#list_posts) | **GET** /{workspaceUuid}/posts | List posts
[**schedule_post**](PostsApi.md#schedule_post) | **POST** /{workspaceUuid}/posts/schedule/{postUuid} | Schedule post
[**update_post**](PostsApi.md#update_post) | **PUT** /{workspaceUuid}/posts/{postUuid} | Update post


# **add_post_to_queue**
> ScheduleResult add_post_to_queue(workspace_uuid, post_uuid)

Add post to queue

Add an existing post to the smart publishing queue.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.schedule_result import ScheduleResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.

    try:
        # Add post to queue
        api_response = api_instance.add_post_to_queue(workspace_uuid, post_uuid)
        print("The response of PostsApi->add_post_to_queue:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->add_post_to_queue: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Queue confirmation |  -  |
**401** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **approve_post**
> ScheduleResult approve_post(workspace_uuid, post_uuid)

Approve post

Approve a post that is pending review.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.schedule_result import ScheduleResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.

    try:
        # Approve post
        api_response = api_instance.approve_post(workspace_uuid, post_uuid)
        print("The response of PostsApi->approve_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->approve_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Approval confirmation |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_post**
> Post create_post(workspace_uuid, post_input)

Create post

Create a new post. Use `schedule: true` with `date` and `time` to schedule, `schedule_now: true` to publish immediately, or `queue: true` to add to the smart publishing queue. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.post import Post
from postboost.models.post_input import PostInput
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_input = postboost.PostInput() # PostInput | 

    try:
        # Create post
        api_response = api_instance.create_post(workspace_uuid, post_input)
        print("The response of PostsApi->create_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->create_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_input** | [**PostInput**](PostInput.md)|  | 

### Return type

[**Post**](Post.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created post |  -  |
**401** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_post**
> DeleteResult delete_post(workspace_uuid, post_uuid, delete_post_request=delete_post_request)

Delete post

Deletes a post. Use `delete_mode` to control whether to also remove the published content from social platforms.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.delete_post_request import DeletePostRequest
from postboost.models.delete_result import DeleteResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.
    delete_post_request = postboost.DeletePostRequest() # DeletePostRequest |  (optional)

    try:
        # Delete post
        api_response = api_instance.delete_post(workspace_uuid, post_uuid, delete_post_request=delete_post_request)
        print("The response of PostsApi->delete_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->delete_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 
 **delete_post_request** | [**DeletePostRequest**](DeletePostRequest.md)|  | [optional] 

### Return type

[**DeleteResult**](DeleteResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Deletion result |  -  |
**401** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_posts_bulk**
> DeleteResult delete_posts_bulk(workspace_uuid, delete_posts_bulk_request)

Delete posts (bulk)

Delete multiple posts at once.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.delete_posts_bulk_request import DeletePostsBulkRequest
from postboost.models.delete_result import DeleteResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    delete_posts_bulk_request = postboost.DeletePostsBulkRequest() # DeletePostsBulkRequest | 

    try:
        # Delete posts (bulk)
        api_response = api_instance.delete_posts_bulk(workspace_uuid, delete_posts_bulk_request)
        print("The response of PostsApi->delete_posts_bulk:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->delete_posts_bulk: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **delete_posts_bulk_request** | [**DeletePostsBulkRequest**](DeletePostsBulkRequest.md)|  | 

### Return type

[**DeleteResult**](DeleteResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Deletion result |  -  |
**401** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_post**
> Post get_post(workspace_uuid, post_uuid)

Get post

Returns a single post with all its versions and associated accounts.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.post import Post
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.

    try:
        # Get post
        api_response = api_instance.get_post(workspace_uuid, post_uuid)
        print("The response of PostsApi->get_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->get_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 

### Return type

[**Post**](Post.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Post details |  -  |
**401** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_posts**
> ListPosts200Response list_posts(workspace_uuid, page=page)

List posts

Returns a paginated list of posts in the workspace.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_posts200_response import ListPosts200Response
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    page = 1 # int |  (optional) (default to 1)

    try:
        # List posts
        api_response = api_instance.list_posts(workspace_uuid, page=page)
        print("The response of PostsApi->list_posts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->list_posts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **page** | **int**|  | [optional] [default to 1]

### Return type

[**ListPosts200Response**](ListPosts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated list of posts |  -  |
**401** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **schedule_post**
> ScheduleResult schedule_post(workspace_uuid, post_uuid, schedule_post_request)

Schedule post

Schedule an existing post. Set `postNow: true` to publish immediately.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.schedule_post_request import SchedulePostRequest
from postboost.models.schedule_result import ScheduleResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.
    schedule_post_request = postboost.SchedulePostRequest() # SchedulePostRequest | 

    try:
        # Schedule post
        api_response = api_instance.schedule_post(workspace_uuid, post_uuid, schedule_post_request)
        print("The response of PostsApi->schedule_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->schedule_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 
 **schedule_post_request** | [**SchedulePostRequest**](SchedulePostRequest.md)|  | 

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Schedule confirmation |  -  |
**401** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_post**
> object update_post(workspace_uuid, post_uuid, post_input)

Update post

Replaces a post's versions, accounts, tags, and scheduling options. The post must not be in a published state.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.post_input import PostInput
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.
    post_input = postboost.PostInput() # PostInput | 

    try:
        # Update post
        api_response = api_instance.update_post(workspace_uuid, post_uuid, post_input)
        print("The response of PostsApi->update_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->update_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 
 **post_input** | [**PostInput**](PostInput.md)|  | 

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
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

