# GetRemoteUploadStatus200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**media** | [**Media**](Media.md) | Present when status is complete. | [optional] 

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


