# postboost.MediaApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**abort_chunked_upload**](MediaApi.md#abort_chunked_upload) | **DELETE** /{workspaceUuid}/media/chunked/{uploadUuid} | Abort chunked upload
[**complete_chunked_upload**](MediaApi.md#complete_chunked_upload) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/complete | Complete chunked upload
[**delete_media_bulk**](MediaApi.md#delete_media_bulk) | **DELETE** /{workspaceUuid}/media | Delete media (bulk)
[**get_media**](MediaApi.md#get_media) | **GET** /{workspaceUuid}/media/{mediaUuid} | Get media
[**get_remote_upload_status**](MediaApi.md#get_remote_upload_status) | **GET** /{workspaceUuid}/media/remote/{downloadId}/status | Get remote upload status
[**initiate_chunked_upload**](MediaApi.md#initiate_chunked_upload) | **POST** /{workspaceUuid}/media/chunked/initiate | Initiate chunked upload
[**initiate_remote_upload**](MediaApi.md#initiate_remote_upload) | **POST** /{workspaceUuid}/media/remote/initiate | Initiate remote upload
[**list_media**](MediaApi.md#list_media) | **GET** /{workspaceUuid}/media | List media
[**update_media**](MediaApi.md#update_media) | **PUT** /{workspaceUuid}/media/{mediaUuid} | Update media
[**upload_chunk**](MediaApi.md#upload_chunk) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/upload | Upload a chunk
[**upload_media**](MediaApi.md#upload_media) | **POST** /{workspaceUuid}/media | Upload media (binary)


# **abort_chunked_upload**
> abort_chunked_upload(workspace_uuid, upload_uuid)

Abort chunked upload

Cancel an in-progress chunked upload session and clean up uploaded chunks.

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
    api_instance = postboost.MediaApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    upload_uuid = 'upload_uuid_example' # str | 

    try:
        # Abort chunked upload
        api_instance.abort_chunked_upload(workspace_uuid, upload_uuid)
    except Exception as e:
        print("Exception when calling MediaApi->abort_chunked_upload: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **upload_uuid** | **str**|  | 

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
**204** | Upload aborted |  -  |
**401** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complete_chunked_upload**
> Media complete_chunked_upload(workspace_uuid, upload_uuid)

Complete chunked upload

Signal that all chunks have been uploaded. Returns the final media object.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.media import Media
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
    api_instance = postboost.MediaApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    upload_uuid = 'upload_uuid_example' # str | 

    try:
        # Complete chunked upload
        api_response = api_instance.complete_chunked_upload(workspace_uuid, upload_uuid)
        print("The response of MediaApi->complete_chunked_upload:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->complete_chunked_upload: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **upload_uuid** | **str**|  | 

### Return type

[**Media**](Media.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Completed media object |  -  |
**401** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_media_bulk**
> object delete_media_bulk(workspace_uuid, delete_media_bulk_request)

Delete media (bulk)

Delete one or more media items by their IDs.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.delete_media_bulk_request import DeleteMediaBulkRequest
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
    api_instance = postboost.MediaApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    delete_media_bulk_request = postboost.DeleteMediaBulkRequest() # DeleteMediaBulkRequest | 

    try:
        # Delete media (bulk)
        api_response = api_instance.delete_media_bulk(workspace_uuid, delete_media_bulk_request)
        print("The response of MediaApi->delete_media_bulk:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->delete_media_bulk: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **delete_media_bulk_request** | [**DeleteMediaBulkRequest**](DeleteMediaBulkRequest.md)|  | 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_media**
> Media get_media(workspace_uuid, media_uuid)

Get media

Returns a single media asset.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.media import Media
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
    api_instance = postboost.MediaApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    media_uuid = 'media_uuid_example' # str | UUID of the media asset.

    try:
        # Get media
        api_response = api_instance.get_media(workspace_uuid, media_uuid)
        print("The response of MediaApi->get_media:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->get_media: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **media_uuid** | **str**| UUID of the media asset. | 

### Return type

[**Media**](Media.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Media asset |  -  |
**401** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_remote_upload_status**
> GetRemoteUploadStatus200Response get_remote_upload_status(workspace_uuid, download_id)

Get remote upload status

Poll the status of an in-progress remote media download.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_remote_upload_status200_response import GetRemoteUploadStatus200Response
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
    api_instance = postboost.MediaApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    download_id = 'download_id_example' # str | 

    try:
        # Get remote upload status
        api_response = api_instance.get_remote_upload_status(workspace_uuid, download_id)
        print("The response of MediaApi->get_remote_upload_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->get_remote_upload_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **download_id** | **str**|  | 

### Return type

[**GetRemoteUploadStatus200Response**](GetRemoteUploadStatus200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Download status |  -  |
**401** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **initiate_chunked_upload**
> InitiateChunkedUpload201Response initiate_chunked_upload(workspace_uuid, initiate_chunked_upload_request)

Initiate chunked upload

Start a chunked upload session for large files. Returns an `upload_uuid`, `chunk_size`, and `total_chunks` to use for subsequent chunk requests. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.initiate_chunked_upload201_response import InitiateChunkedUpload201Response
from postboost.models.initiate_chunked_upload_request import InitiateChunkedUploadRequest
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
    api_instance = postboost.MediaApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    initiate_chunked_upload_request = postboost.InitiateChunkedUploadRequest() # InitiateChunkedUploadRequest | 

    try:
        # Initiate chunked upload
        api_response = api_instance.initiate_chunked_upload(workspace_uuid, initiate_chunked_upload_request)
        print("The response of MediaApi->initiate_chunked_upload:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->initiate_chunked_upload: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **initiate_chunked_upload_request** | [**InitiateChunkedUploadRequest**](InitiateChunkedUploadRequest.md)|  | 

### Return type

[**InitiateChunkedUpload201Response**](InitiateChunkedUpload201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Chunked upload session details |  -  |
**401** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **initiate_remote_upload**
> InitiateRemoteUpload201Response initiate_remote_upload(workspace_uuid, initiate_remote_upload_request)

Initiate remote upload

Download a file from a remote URL into the media library. For small files the media object is returned immediately. For large files a `download_id` is returned — poll the status endpoint. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.initiate_remote_upload201_response import InitiateRemoteUpload201Response
from postboost.models.initiate_remote_upload_request import InitiateRemoteUploadRequest
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
    api_instance = postboost.MediaApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    initiate_remote_upload_request = postboost.InitiateRemoteUploadRequest() # InitiateRemoteUploadRequest | 

    try:
        # Initiate remote upload
        api_response = api_instance.initiate_remote_upload(workspace_uuid, initiate_remote_upload_request)
        print("The response of MediaApi->initiate_remote_upload:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->initiate_remote_upload: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **initiate_remote_upload_request** | [**InitiateRemoteUploadRequest**](InitiateRemoteUploadRequest.md)|  | 

### Return type

[**InitiateRemoteUpload201Response**](InitiateRemoteUpload201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Media object or download job |  -  |
**401** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_media**
> ListMedia200Response list_media(workspace_uuid, page=page)

List media

Returns a paginated list of media assets in the workspace library.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_media200_response import ListMedia200Response
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
    api_instance = postboost.MediaApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    page = 1 # int | Page number (20 items per page). (optional) (default to 1)

    try:
        # List media
        api_response = api_instance.list_media(workspace_uuid, page=page)
        print("The response of MediaApi->list_media:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->list_media: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **page** | **int**| Page number (20 items per page). | [optional] [default to 1]

### Return type

[**ListMedia200Response**](ListMedia200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated list of media |  -  |
**401** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_media**
> object update_media(workspace_uuid, media_uuid, update_media_request)

Update media

Update the alt text of a media asset.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.update_media_request import UpdateMediaRequest
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
    api_instance = postboost.MediaApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    media_uuid = 'media_uuid_example' # str | UUID of the media asset.
    update_media_request = postboost.UpdateMediaRequest() # UpdateMediaRequest | 

    try:
        # Update media
        api_response = api_instance.update_media(workspace_uuid, media_uuid, update_media_request)
        print("The response of MediaApi->update_media:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->update_media: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **media_uuid** | **str**| UUID of the media asset. | 
 **update_media_request** | [**UpdateMediaRequest**](UpdateMediaRequest.md)|  | 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_chunk**
> UploadChunk201Response upload_chunk(workspace_uuid, upload_uuid, chunk, chunk_index)

Upload a chunk

Upload a single chunk of a chunked upload session.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.upload_chunk201_response import UploadChunk201Response
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
    api_instance = postboost.MediaApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    upload_uuid = 'upload_uuid_example' # str | 
    chunk = None # bytearray | 
    chunk_index = 56 # int | Zero-based index of this chunk.

    try:
        # Upload a chunk
        api_response = api_instance.upload_chunk(workspace_uuid, upload_uuid, chunk, chunk_index)
        print("The response of MediaApi->upload_chunk:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->upload_chunk: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **upload_uuid** | **str**|  | 
 **chunk** | **bytearray**|  | 
 **chunk_index** | **int**| Zero-based index of this chunk. | 

### Return type

[**UploadChunk201Response**](UploadChunk201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Chunk received |  -  |
**401** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_media**
> Media upload_media(workspace_uuid, file, alt_text=alt_text)

Upload media (binary)

Upload a file directly as multipart form data.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.media import Media
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
    api_instance = postboost.MediaApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    file = None # bytearray | The file to upload.
    alt_text = 'alt_text_example' # str | Alternative text for accessibility. (optional)

    try:
        # Upload media (binary)
        api_response = api_instance.upload_media(workspace_uuid, file, alt_text=alt_text)
        print("The response of MediaApi->upload_media:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->upload_media: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **file** | **bytearray**| The file to upload. | 
 **alt_text** | **str**| Alternative text for accessibility. | [optional] 

### Return type

[**Media**](Media.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Uploaded media object |  -  |
**401** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

