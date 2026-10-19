# GetRemoteUploadStatus200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | 
**progress** | **int** | Percent done. It stays &#x60;0&#x60; until the file is stored and is &#x60;100&#x60; once &#x60;status&#x60; is &#x60;completed&#x60;, so poll on &#x60;status&#x60;. | 
**media** | [**Media**](Media.md) | Present when &#x60;status&#x60; is &#x60;completed&#x60; (absent if the item was deleted before this poll). | [optional] 
**error** | **str** | Why the download failed. Present when &#x60;status&#x60; is &#x60;failed&#x60;. | [optional] 

## Example

```python
from postboost.models.get_remote_upload_status200_response import GetRemoteUploadStatus200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetRemoteUploadStatus200Response from a JSON string
get_remote_upload_status200_response_instance = GetRemoteUploadStatus200Response.from_json(json)
# print the JSON string representation of the object
print(GetRemoteUploadStatus200Response.to_json())

# convert the object into a dict
get_remote_upload_status200_response_dict = get_remote_upload_status200_response_instance.to_dict()
# create an instance of GetRemoteUploadStatus200Response from a dict
get_remote_upload_status200_response_from_dict = GetRemoteUploadStatus200Response.from_dict(get_remote_upload_status200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


