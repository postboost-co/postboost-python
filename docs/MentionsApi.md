# postboost.MentionsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_mention**](MentionsApi.md#create_mention) | **POST** /{workspaceUuid}/mentions | Create mention
[**delete_mention**](MentionsApi.md#delete_mention) | **DELETE** /{workspaceUuid}/mentions/{mentionId} | Delete mention
[**get_mention**](MentionsApi.md#get_mention) | **GET** /{workspaceUuid}/mentions/{mentionId} | Get mention
[**list_mentions**](MentionsApi.md#list_mentions) | **GET** /{workspaceUuid}/mentions | List mentions
[**update_mention**](MentionsApi.md#update_mention) | **PUT** /{workspaceUuid}/mentions/{mentionId} | Update mention


# **create_mention**
> CreateMention201Response create_mention(workspace_uuid, mention_input, idempotency_key=idempotency_key)

Create mention

Adds a person or page to the mention book. When one of the submitted identities already belongs to a stored mention, that mention is reused and the identities are added to it (status `200` instead of `201`). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_mention201_response import CreateMention201Response
from postboost.models.mention_input import MentionInput
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
    api_instance = postboost.MentionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    mention_input = postboost.MentionInput() # MentionInput | 
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)

    try:
        # Create mention
        api_response = api_instance.create_mention(workspace_uuid, mention_input, idempotency_key=idempotency_key)
        print("The response of MentionsApi->create_mention:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MentionsApi->create_mention: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **mention_input** | [**MentionInput**](MentionInput.md)|  | 
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 

### Return type

[**CreateMention201Response**](CreateMention201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created mention |  -  |
**200** | Existing mention reused |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_mention**
> object delete_mention(workspace_uuid, mention_id)

Delete mention

Removes a mention from the mention book. `success` is false when nothing was deleted.

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
    api_instance = postboost.MentionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    mention_id = 'mention_id_example' # str | The mention's `id` (a UUID).

    try:
        # Delete mention
        api_response = api_instance.delete_mention(workspace_uuid, mention_id)
        print("The response of MentionsApi->delete_mention:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MentionsApi->delete_mention: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **mention_id** | **str**| The mention&#39;s &#x60;id&#x60; (a UUID). | 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_mention**
> CreateMention201Response get_mention(workspace_uuid, mention_id)

Get mention

Returns a single mention with its identities.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_mention201_response import CreateMention201Response
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
    api_instance = postboost.MentionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    mention_id = 'mention_id_example' # str | The mention's `id` (a UUID).

    try:
        # Get mention
        api_response = api_instance.get_mention(workspace_uuid, mention_id)
        print("The response of MentionsApi->get_mention:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MentionsApi->get_mention: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **mention_id** | **str**| The mention&#39;s &#x60;id&#x60; (a UUID). | 

### Return type

[**CreateMention201Response**](CreateMention201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Mention |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_mentions**
> ListMentions200Response list_mentions(workspace_uuid, q=q, per_page=per_page, page=page)

List mentions

Returns a paginated list of the workspace's mention book, ranked, with each entry's network identities.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_mentions200_response import ListMentions200Response
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
    api_instance = postboost.MentionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    q = 'q_example' # str | Search keyword. (optional)
    per_page = 25 # int |  (optional) (default to 25)
    page = 1 # int |  (optional) (default to 1)

    try:
        # List mentions
        api_response = api_instance.list_mentions(workspace_uuid, q=q, per_page=per_page, page=page)
        print("The response of MentionsApi->list_mentions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MentionsApi->list_mentions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **q** | **str**| Search keyword. | [optional] 
 **per_page** | **int**|  | [optional] [default to 25]
 **page** | **int**|  | [optional] [default to 1]

### Return type

[**ListMentions200Response**](ListMentions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated list of mentions |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_mention**
> CreateMention201Response update_mention(workspace_uuid, mention_id, mention_input)

Update mention

Replaces the mention's name, avatar and identities. Identities for providers not in the payload are removed. An identity already held by another mention returns `422`.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_mention201_response import CreateMention201Response
from postboost.models.mention_input import MentionInput
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
    api_instance = postboost.MentionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    mention_id = 'mention_id_example' # str | The mention's `id` (a UUID).
    mention_input = postboost.MentionInput() # MentionInput | 

    try:
        # Update mention
        api_response = api_instance.update_mention(workspace_uuid, mention_id, mention_input)
        print("The response of MentionsApi->update_mention:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MentionsApi->update_mention: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **mention_id** | **str**| The mention&#39;s &#x60;id&#x60; (a UUID). | 
 **mention_input** | [**MentionInput**](MentionInput.md)|  | 

### Return type

[**CreateMention201Response**](CreateMention201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated mention |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

