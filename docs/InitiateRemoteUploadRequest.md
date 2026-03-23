# InitiateRemoteUploadRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | URL of the remote file to download. | 
**alt_text** | **str** |  | [optional] 

## Example

```python
from postboost.models.initiate_remote_upload_request import InitiateRemoteUploadRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InitiateRemoteUploadRequest from a JSON string
initiate_remote_upload_request_instance = InitiateRemoteUploadRequest.from_json(json)
# print the JSON string representation of the object
print(InitiateRemoteUploadRequest.to_json())

# convert the object into a dict
initiate_remote_upload_request_dict = initiate_remote_upload_request_instance.to_dict()
# create an instance of InitiateRemoteUploadRequest from a dict
initiate_remote_upload_request_from_dict = InitiateRemoteUploadRequest.from_dict(initiate_remote_upload_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


