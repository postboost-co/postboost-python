# UploadChunk201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**received** | **int** | Number of chunks received so far. | [optional] 

## Example

```python
from postboost.models.upload_chunk201_response import UploadChunk201Response

# TODO update the JSON string below
json = "{}"
# create an instance of UploadChunk201Response from a JSON string
upload_chunk201_response_instance = UploadChunk201Response.from_json(json)
# print the JSON string representation of the object
print(UploadChunk201Response.to_json())

# convert the object into a dict
upload_chunk201_response_dict = upload_chunk201_response_instance.to_dict()
# create an instance of UploadChunk201Response from a dict
upload_chunk201_response_from_dict = UploadChunk201Response.from_dict(upload_chunk201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


