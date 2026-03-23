# InitiateRemoteUpload200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**uuid** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**mime_type** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**thumb_url** | **str** |  | [optional] 
**is_video** | **bool** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**download_id** | **str** |  | [optional] 

## Example

```python
from postboost.models.initiate_remote_upload200_response import InitiateRemoteUpload200Response

# TODO update the JSON string below
json = "{}"
# create an instance of InitiateRemoteUpload200Response from a JSON string
initiate_remote_upload200_response_instance = InitiateRemoteUpload200Response.from_json(json)
# print the JSON string representation of the object
print(InitiateRemoteUpload200Response.to_json())

# convert the object into a dict
initiate_remote_upload200_response_dict = initiate_remote_upload200_response_instance.to_dict()
# create an instance of InitiateRemoteUpload200Response from a dict
initiate_remote_upload200_response_from_dict = InitiateRemoteUpload200Response.from_dict(initiate_remote_upload200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


