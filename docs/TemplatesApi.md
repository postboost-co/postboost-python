# postboost.TemplatesApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_template**](TemplatesApi.md#create_template) | **POST** /{workspaceUuid}/templates | Create a template
[**delete_template**](TemplatesApi.md#delete_template) | **DELETE** /{workspaceUuid}/templates/{templateId} | Delete a template
[**get_template**](TemplatesApi.md#get_template) | **GET** /{workspaceUuid}/templates/{templateId} | Get a template
[**list_templates**](TemplatesApi.md#list_templates) | **GET** /{workspaceUuid}/templates | List templates
[**update_template**](TemplatesApi.md#update_template) | **PUT** /{workspaceUuid}/templates/{templateId} | Update a template


# **create_template**
> CreateTemplate201Response create_template(workspace_uuid, template_input)

Create a template

Creates a post template: a name and one or more content items (body plus media ids from the media library). Admins and members only (not viewers). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_template201_response import CreateTemplate201Response
from postboost.models.template_input import TemplateInput
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
    api_instance = postboost.TemplatesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    template_input = postboost.TemplateInput() # TemplateInput | 

    try:
        # Create a template
        api_response = api_instance.create_template(workspace_uuid, template_input)
        print("The response of TemplatesApi->create_template:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TemplatesApi->create_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **template_input** | [**TemplateInput**](TemplateInput.md)|  | 

### Return type

[**CreateTemplate201Response**](CreateTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The new template |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_template**
> delete_template(workspace_uuid, template_id)

Delete a template

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
    api_instance = postboost.TemplatesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    template_id = 'template_id_example' # str | The template `id`.

    try:
        # Delete a template
        api_instance.delete_template(workspace_uuid, template_id)
    except Exception as e:
        print("Exception when calling TemplatesApi->delete_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **template_id** | **str**| The template &#x60;id&#x60;. | 

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

# **get_template**
> CreateTemplate201Response get_template(workspace_uuid, template_id)

Get a template

One template. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_template201_response import CreateTemplate201Response
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
    api_instance = postboost.TemplatesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    template_id = 'template_id_example' # str | The template `id`.

    try:
        # Get a template
        api_response = api_instance.get_template(workspace_uuid, template_id)
        print("The response of TemplatesApi->get_template:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TemplatesApi->get_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **template_id** | **str**| The template &#x60;id&#x60;. | 

### Return type

[**CreateTemplate201Response**](CreateTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The template |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_templates**
> ListTemplates200Response list_templates(workspace_uuid, page=page, per_page=per_page)

List templates

Post templates of the workspace, newest first. The same templates as the Templates page in the app. Paginated with `page` and `per_page` (default 100). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_templates200_response import ListTemplates200Response
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
    api_instance = postboost.TemplatesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    page = 1 # int | Page number (1-based). (optional) (default to 1)
    per_page = 100 # int | Items per page, 1-100. (optional) (default to 100)

    try:
        # List templates
        api_response = api_instance.list_templates(workspace_uuid, page=page, per_page=per_page)
        print("The response of TemplatesApi->list_templates:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TemplatesApi->list_templates: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **page** | **int**| Page number (1-based). | [optional] [default to 1]
 **per_page** | **int**| Items per page, 1-100. | [optional] [default to 100]

### Return type

[**ListTemplates200Response**](ListTemplates200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Templates, paginated (&#x60;links&#x60; and &#x60;meta&#x60; as on the other list endpoints) |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_template**
> CreateTemplate201Response update_template(workspace_uuid, template_id, template_input)

Update a template

Replaces the name and content of a template. Admins and members only (not viewers). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_template201_response import CreateTemplate201Response
from postboost.models.template_input import TemplateInput
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
    api_instance = postboost.TemplatesApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    template_id = 'template_id_example' # str | The template `id`.
    template_input = postboost.TemplateInput() # TemplateInput | 

    try:
        # Update a template
        api_response = api_instance.update_template(workspace_uuid, template_id, template_input)
        print("The response of TemplatesApi->update_template:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TemplatesApi->update_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **template_id** | **str**| The template &#x60;id&#x60;. | 
 **template_input** | [**TemplateInput**](TemplateInput.md)|  | 

### Return type

[**CreateTemplate201Response**](CreateTemplate201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated template |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

