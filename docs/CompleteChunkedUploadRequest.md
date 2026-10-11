# CompleteChunkedUploadRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**alt_text** | **str** |  | [optional] 
**folder** | **str** | UUID of the media folder to file the item in. Omit or null for the library root. | [optional] 

## Example

```python
from postboost.models.complete_chunked_upload_request import CompleteChunkedUploadRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CompleteChunkedUploadRequest from a JSON string
complete_chunked_upload_request_instance = CompleteChunkedUploadRequest.from_json(json)
# print the JSON string representation of the object
print(CompleteChunkedUploadRequest.to_json())

# convert the object into a dict
complete_chunked_upload_request_dict = complete_chunked_upload_request_instance.to_dict()
# create an instance of CompleteChunkedUploadRequest from a dict
complete_chunked_upload_request_from_dict = CompleteChunkedUploadRequest.from_dict(complete_chunked_upload_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


