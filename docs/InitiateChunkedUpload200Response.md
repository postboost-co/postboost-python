# InitiateChunkedUpload200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**upload_uuid** | **str** |  | [optional] 
**chunk_size** | **int** |  | [optional] 
**total_chunks** | **int** |  | [optional] 

## Example

```python
from postboost.models.initiate_chunked_upload200_response import InitiateChunkedUpload200Response

# TODO update the JSON string below
json = "{}"
# create an instance of InitiateChunkedUpload200Response from a JSON string
initiate_chunked_upload200_response_instance = InitiateChunkedUpload200Response.from_json(json)
# print the JSON string representation of the object
print(InitiateChunkedUpload200Response.to_json())

# convert the object into a dict
initiate_chunked_upload200_response_dict = initiate_chunked_upload200_response_instance.to_dict()
# create an instance of InitiateChunkedUpload200Response from a dict
initiate_chunked_upload200_response_from_dict = InitiateChunkedUpload200Response.from_dict(initiate_chunked_upload200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


