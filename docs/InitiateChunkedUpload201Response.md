# InitiateChunkedUpload201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**upload_uuid** | **str** |  | [optional] 
**chunk_size** | **int** |  | [optional] 
**total_chunks** | **int** |  | [optional] 

## Example

```python
from postboost.models.initiate_chunked_upload201_response import InitiateChunkedUpload201Response

# TODO update the JSON string below
json = "{}"
# create an instance of InitiateChunkedUpload201Response from a JSON string
initiate_chunked_upload201_response_instance = InitiateChunkedUpload201Response.from_json(json)
# print the JSON string representation of the object
print(InitiateChunkedUpload201Response.to_json())

# convert the object into a dict
initiate_chunked_upload201_response_dict = initiate_chunked_upload201_response_instance.to_dict()
# create an instance of InitiateChunkedUpload201Response from a dict
initiate_chunked_upload201_response_from_dict = InitiateChunkedUpload201Response.from_dict(initiate_chunked_upload201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


