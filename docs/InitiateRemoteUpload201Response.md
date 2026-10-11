# InitiateRemoteUpload201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**uuid** | **str** |  | 
**name** | **str** |  | 
**mime_type** | **str** |  | 
**type** | **str** |  | 
**url** | **str** |  | 
**thumb_url** | **str** |  | [optional] 
**is_video** | **bool** |  | 
**is_processing** | **bool** | True while an uploaded video is still being converted. | [optional] 
**width** | **int** | Width in pixels, when stored. | [optional] 
**height** | **int** | Height in pixels, when stored. | [optional] 
**duration_ms** | **int** | Video duration in milliseconds; null for images or videos not read yet. | [optional] 
**size** | **int** | File size in bytes. | [optional] 
**alt_text** | **str** |  | [optional] 
**folder** | [**MediaFolderRef**](MediaFolderRef.md) |  | [optional] 
**created_at** | **datetime** |  | 
**download_id** | **str** |  | [optional] 

## Example

```python
from postboost.models.initiate_remote_upload201_response import InitiateRemoteUpload201Response

# TODO update the JSON string below
json = "{}"
# create an instance of InitiateRemoteUpload201Response from a JSON string
initiate_remote_upload201_response_instance = InitiateRemoteUpload201Response.from_json(json)
# print the JSON string representation of the object
print(InitiateRemoteUpload201Response.to_json())

# convert the object into a dict
initiate_remote_upload201_response_dict = initiate_remote_upload201_response_instance.to_dict()
# create an instance of InitiateRemoteUpload201Response from a dict
initiate_remote_upload201_response_from_dict = InitiateRemoteUpload201Response.from_dict(initiate_remote_upload201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


