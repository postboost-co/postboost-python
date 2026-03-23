# postboost.TagsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_tag**](TagsApi.md#create_tag) | **POST** /{workspaceUuid}/tags | Create tag
[**delete_tag**](TagsApi.md#delete_tag) | **DELETE** /{workspaceUuid}/tags/{tagUuid} | Delete tag
[**get_tag**](TagsApi.md#get_tag) | **GET** /{workspaceUuid}/tags/{tagUuid} | Get tag
[**list_tags**](TagsApi.md#list_tags) | **GET** /{workspaceUuid}/tags | List tags
[**update_tag**](TagsApi.md#update_tag) | **PUT** /{workspaceUuid}/tags/{tagUuid} | Update tag


# **create_tag**
> Tag create_tag(workspace_uuid, tag_input)

Create tag

Creates a new color-coded tag in the workspace for organizing posts.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.tag import Tag
from postboost.models.tag_input import TagInput
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
    api_instance = postboost.TagsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    tag_input = postboost.TagInput() # TagInput | 

    try:
        # Create tag
        api_response = api_instance.create_tag(workspace_uuid, tag_input)
        print("The response of TagsApi->create_tag:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TagsApi->create_tag: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **tag_input** | [**TagInput**](TagInput.md)|  | 

### Return type

[**Tag**](Tag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created tag |  -  |
**401** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_tag**
> object delete_tag(workspace_uuid, tag_uuid)

Delete tag

Permanently deletes a tag. Posts that had this tag attached are unaffected.

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
    api_instance = postboost.TagsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    tag_uuid = 'tag_uuid_example' # str | UUID of the tag.

    try:
        # Delete tag
        api_response = api_instance.delete_tag(workspace_uuid, tag_uuid)
        print("The response of TagsApi->delete_tag:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TagsApi->delete_tag: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **tag_uuid** | **str**| UUID of the tag. | 

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
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tag**
> Tag get_tag(workspace_uuid, tag_uuid)

Get tag

Returns a single tag by UUID.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.tag import Tag
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
    api_instance = postboost.TagsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    tag_uuid = 'tag_uuid_example' # str | UUID of the tag.

    try:
        # Get tag
        api_response = api_instance.get_tag(workspace_uuid, tag_uuid)
        print("The response of TagsApi->get_tag:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TagsApi->get_tag: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **tag_uuid** | **str**| UUID of the tag. | 

### Return type

[**Tag**](Tag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Tag details |  -  |
**401** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_tags**
> ListTags200Response list_tags(workspace_uuid)

List tags

Returns all tags defined in the workspace.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_tags200_response import ListTags200Response
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
    api_instance = postboost.TagsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # List tags
        api_response = api_instance.list_tags(workspace_uuid)
        print("The response of TagsApi->list_tags:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TagsApi->list_tags: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**ListTags200Response**](ListTags200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of tags |  -  |
**401** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_tag**
> object update_tag(workspace_uuid, tag_uuid, tag_input)

Update tag

Updates a tag's name or color.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.tag_input import TagInput
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
    api_instance = postboost.TagsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    tag_uuid = 'tag_uuid_example' # str | UUID of the tag.
    tag_input = postboost.TagInput() # TagInput | 

    try:
        # Update tag
        api_response = api_instance.update_tag(workspace_uuid, tag_uuid, tag_input)
        print("The response of TagsApi->update_tag:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TagsApi->update_tag: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **tag_uuid** | **str**| UUID of the tag. | 
 **tag_input** | [**TagInput**](TagInput.md)|  | 

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

