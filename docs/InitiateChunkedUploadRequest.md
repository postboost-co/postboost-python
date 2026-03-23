# InitiateChunkedUploadRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**filename** | **str** |  | 
**mime_type** | **str** |  | 
**total_size** | **int** | Total file size in bytes. | 

## Example

```python
from postboost.models.initiate_chunked_upload_request import InitiateChunkedUploadRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InitiateChunkedUploadRequest from a JSON string
initiate_chunked_upload_request_instance = InitiateChunkedUploadRequest.from_json(json)
# print the JSON string representation of the object
print(InitiateChunkedUploadRequest.to_json())

# convert the object into a dict
initiate_chunked_upload_request_dict = initiate_chunked_upload_request_instance.to_dict()
# create an instance of InitiateChunkedUploadRequest from a dict
initiate_chunked_upload_request_from_dict = InitiateChunkedUploadRequest.from_dict(initiate_chunked_upload_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


