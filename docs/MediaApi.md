# postboost.MediaApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**abort_chunked_upload**](MediaApi.md#abort_chunked_upload) | **DELETE** /{workspaceUuid}/media/chunked/{uploadUuid} | Abort chunked upload
[**complete_chunked_upload**](MediaApi.md#complete_chunked_upload) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/complete | Complete chunked upload
[**create_media_folder**](MediaApi.md#create_media_folder) | **POST** /{workspaceUuid}/media/folders | Create media folder
[**delete_media_bulk**](MediaApi.md#delete_media_bulk) | **DELETE** /{workspaceUuid}/media | Delete media (bulk)
[**delete_media_folder**](MediaApi.md#delete_media_folder) | **DELETE** /{workspaceUuid}/media/folders/{folderUuid} | Delete media folder
[**get_media**](MediaApi.md#get_media) | **GET** /{workspaceUuid}/media/{mediaUuid} | Get media
[**get_remote_upload_status**](MediaApi.md#get_remote_upload_status) | **GET** /{workspaceUuid}/media/remote/{downloadId}/status | Get remote upload status
[**initiate_chunked_upload**](MediaApi.md#initiate_chunked_upload) | **POST** /{workspaceUuid}/media/chunked/initiate | Initiate chunked upload
[**initiate_remote_upload**](MediaApi.md#initiate_remote_upload) | **POST** /{workspaceUuid}/media/remote/initiate | Initiate remote upload
[**list_media**](MediaApi.md#list_media) | **GET** /{workspaceUuid}/media | List media
[**list_media_folders**](MediaApi.md#list_media_folders) | **GET** /{workspaceUuid}/media/folders | List media folders
[**update_media**](MediaApi.md#update_media) | **PUT** /{workspaceUuid}/media/{mediaUuid} | Update media
[**update_media_folder**](MediaApi.md#update_media_folder) | **PUT** /{workspaceUuid}/media/folders/{folderUuid} | Update media folder
[**upload_chunk**](MediaApi.md#upload_chunk) | **POST** /{workspaceUuid}/media/chunked/{uploadUuid}/upload | Upload a chunk
[**upload_media**](MediaApi.md#upload_media) | **POST** /{workspaceUuid}/media | Upload media (binary)
[**upload_media_base64**](MediaApi.md#upload_media_base64) | **POST** /{workspaceUuid}/media/base64 | Upload media (base64 JSON)


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
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complete_chunked_upload**
> Media complete_chunked_upload(workspace_uuid, upload_uuid, complete_chunked_upload_request=complete_chunked_upload_request)

Complete chunked upload

Signal that all chunks have been uploaded. Returns the final media object. A video may come back with `is_processing` set to `true` while its conversion runs.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.complete_chunked_upload_request import CompleteChunkedUploadRequest
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
    complete_chunked_upload_request = postboost.CompleteChunkedUploadRequest() # CompleteChunkedUploadRequest |  (optional)

    try:
        # Complete chunked upload
        api_response = api_instance.complete_chunked_upload(workspace_uuid, upload_uuid, complete_chunked_upload_request=complete_chunked_upload_request)
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
 **complete_chunked_upload_request** | [**CompleteChunkedUploadRequest**](CompleteChunkedUploadRequest.md)|  | [optional] 

### Return type

[**Media**](Media.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Completed media object |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_media_folder**
> MediaFolder create_media_folder(workspace_uuid, create_media_folder_request, idempotency_key=idempotency_key)

Create media folder

Creates a folder at the top level or under `parent`. The name must be unique among its siblings.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_media_folder_request import CreateMediaFolderRequest
from postboost.models.media_folder import MediaFolder
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
    create_media_folder_request = postboost.CreateMediaFolderRequest() # CreateMediaFolderRequest | 
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)

    try:
        # Create media folder
        api_response = api_instance.create_media_folder(workspace_uuid, create_media_folder_request, idempotency_key=idempotency_key)
        print("The response of MediaApi->create_media_folder:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->create_media_folder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **create_media_folder_request** | [**CreateMediaFolderRequest**](CreateMediaFolderRequest.md)|  | 
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 

### Return type

[**MediaFolder**](MediaFolder.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created folder |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_media_bulk**
> object delete_media_bulk(workspace_uuid, delete_media_bulk_request)

Delete media (bulk)

Delete one or more media items by their numeric IDs or UUIDs (both may be mixed, up to 500 per request).

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
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_media_folder**
> object delete_media_folder(workspace_uuid, folder_uuid, delete_media_folder_request=delete_media_folder_request)

Delete media folder

Deletes a folder. By default its media and sub-folders move up to the folder's parent; with `delete_media` set to true every media item below the folder is deleted as well.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.delete_media_folder_request import DeleteMediaFolderRequest
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
    folder_uuid = 'folder_uuid_example' # str | UUID of the media folder.
    delete_media_folder_request = postboost.DeleteMediaFolderRequest() # DeleteMediaFolderRequest |  (optional)

    try:
        # Delete media folder
        api_response = api_instance.delete_media_folder(workspace_uuid, folder_uuid, delete_media_folder_request=delete_media_folder_request)
        print("The response of MediaApi->delete_media_folder:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->delete_media_folder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **folder_uuid** | **str**| UUID of the media folder. | 
 **delete_media_folder_request** | [**DeleteMediaFolderRequest**](DeleteMediaFolderRequest.md)|  | [optional] 

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
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

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
**403** |  |  -  |
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
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **initiate_chunked_upload**
> InitiateChunkedUpload201Response initiate_chunked_upload(workspace_uuid, initiate_chunked_upload_request, idempotency_key=idempotency_key)

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
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)

    try:
        # Initiate chunked upload
        api_response = api_instance.initiate_chunked_upload(workspace_uuid, initiate_chunked_upload_request, idempotency_key=idempotency_key)
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
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 

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
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **initiate_remote_upload**
> InitiateRemoteUpload201Response initiate_remote_upload(workspace_uuid, initiate_remote_upload_request, idempotency_key=idempotency_key)

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
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)

    try:
        # Initiate remote upload
        api_response = api_instance.initiate_remote_upload(workspace_uuid, initiate_remote_upload_request, idempotency_key=idempotency_key)
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
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 

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
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_media**
> ListMedia200Response list_media(workspace_uuid, page=page, limit=limit, folder=folder, mime_types=mime_types, type=type, keyword=keyword, usage=usage, favorite=favorite, sort=sort)

List media

Returns a paginated list of media assets in the workspace library. Without `folder` every item is listed, whatever folder it is filed in. A `keyword` search always looks at the whole library and ignores `folder` and `favorite`. 

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
    page = 1 # int | Page number. (optional) (default to 1)
    limit = 50 # int | Items per page. Values below 1 fall back to 50; values above 100 are capped at 100. (optional) (default to 50)
    folder = 'folder_example' # str | Media folder UUID, or `root` for items not filed in any folder. (optional)
    mime_types = ['mime_types_example'] # List[str] | Only these MIME types (for example `image/png`). (optional)
    type = 'type_example' # str | Only this media type. (optional)
    keyword = 'keyword_example' # str | Search media by name. (optional)
    usage = 'usage_example' # str | Filter by how the media is used in posts. (optional)
    favorite = True # bool | When `true`, only media the caller marked as favorite. (optional)
    sort = newest # str |  (optional) (default to newest)

    try:
        # List media
        api_response = api_instance.list_media(workspace_uuid, page=page, limit=limit, folder=folder, mime_types=mime_types, type=type, keyword=keyword, usage=usage, favorite=favorite, sort=sort)
        print("The response of MediaApi->list_media:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->list_media: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **page** | **int**| Page number. | [optional] [default to 1]
 **limit** | **int**| Items per page. Values below 1 fall back to 50; values above 100 are capped at 100. | [optional] [default to 50]
 **folder** | **str**| Media folder UUID, or &#x60;root&#x60; for items not filed in any folder. | [optional] 
 **mime_types** | [**List[str]**](str.md)| Only these MIME types (for example &#x60;image/png&#x60;). | [optional] 
 **type** | **str**| Only this media type. | [optional] 
 **keyword** | **str**| Search media by name. | [optional] 
 **usage** | **str**| Filter by how the media is used in posts. | [optional] 
 **favorite** | **bool**| When &#x60;true&#x60;, only media the caller marked as favorite. | [optional] 
 **sort** | **str**|  | [optional] [default to newest]

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
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_media_folders**
> ListMediaFolders200Response list_media_folders(workspace_uuid)

List media folders

Returns the whole folder tree of the media library in one response (not paginated). Rebuild the tree from each folder's `parent`.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_media_folders200_response import ListMediaFolders200Response
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

    try:
        # List media folders
        api_response = api_instance.list_media_folders(workspace_uuid)
        print("The response of MediaApi->list_media_folders:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->list_media_folders: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**ListMediaFolders200Response**](ListMediaFolders200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | All media folders |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_media**
> object update_media(workspace_uuid, media_uuid, update_media_request)

Update media

Update the name, alt text, or folder of a media asset. Only the keys present in the body are written. Sending `folder: null` moves the item to the library root; omitting `folder` leaves it where it is. 

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
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_media_folder**
> MediaFolder update_media_folder(workspace_uuid, folder_uuid, media_folder_input)

Update media folder

Renames a folder and/or moves it. Sending `parent` moves the folder (null = top level); omitting it keeps the current parent. A folder cannot be moved into itself or one of its descendants.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.media_folder import MediaFolder
from postboost.models.media_folder_input import MediaFolderInput
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
    folder_uuid = 'folder_uuid_example' # str | UUID of the media folder.
    media_folder_input = postboost.MediaFolderInput() # MediaFolderInput | 

    try:
        # Update media folder
        api_response = api_instance.update_media_folder(workspace_uuid, folder_uuid, media_folder_input)
        print("The response of MediaApi->update_media_folder:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->update_media_folder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **folder_uuid** | **str**| UUID of the media folder. | 
 **media_folder_input** | [**MediaFolderInput**](MediaFolderInput.md)|  | 

### Return type

[**MediaFolder**](MediaFolder.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated folder |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

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
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_media**
> Media upload_media(workspace_uuid, file, idempotency_key=idempotency_key, alt_text=alt_text, folder=folder)

Upload media (binary)

Upload a file directly as multipart form data. Images and videos, plus a PDF (up to 100 MB) for LinkedIn document posts: a post that attaches a PDF must have it as the only media item and may only go to LinkedIn profiles and pages. 

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
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)
    alt_text = 'alt_text_example' # str | Alternative text for accessibility. (optional)
    folder = 'folder_example' # str | UUID of the media folder to file the upload in. Omit or null for the library root. (optional)

    try:
        # Upload media (binary)
        api_response = api_instance.upload_media(workspace_uuid, file, idempotency_key=idempotency_key, alt_text=alt_text, folder=folder)
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
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 
 **alt_text** | **str**| Alternative text for accessibility. | [optional] 
 **folder** | **str**| UUID of the media folder to file the upload in. Omit or null for the library root. | [optional] 

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
**201** | Uploaded media object. A video may come back with &#x60;is_processing&#x60; set to &#x60;true&#x60; while its conversion runs. |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_media_base64**
> Media upload_media_base64(workspace_uuid, media_base64_input, idempotency_key=idempotency_key)

Upload media (base64 JSON)

Upload a file as base64 inside a JSON body, for agents and tools that cannot send multipart form data. The decoded file is checked exactly like `POST media` (allowed types and size limits; a PDF is accepted for LinkedIn document posts). Decoded size is capped at 20 MB; for larger files use remote upload by URL or chunked upload. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.media import Media
from postboost.models.media_base64_input import MediaBase64Input
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
    media_base64_input = postboost.MediaBase64Input() # MediaBase64Input | 
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)

    try:
        # Upload media (base64 JSON)
        api_response = api_instance.upload_media_base64(workspace_uuid, media_base64_input, idempotency_key=idempotency_key)
        print("The response of MediaApi->upload_media_base64:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MediaApi->upload_media_base64: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **media_base64_input** | [**MediaBase64Input**](MediaBase64Input.md)|  | 
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 

### Return type

[**Media**](Media.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Uploaded media object |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

