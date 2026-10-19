# InitiateRemoteUpload200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** | &#x60;completed&#x60; and &#x60;failed&#x60; are final; &#x60;pending&#x60; means the file downloads in the background. | 
**media** | [**Media**](Media.md) | Present when &#x60;status&#x60; is &#x60;completed&#x60;. This copy has no &#x60;size&#x60;; &#x60;getMedia&#x60; returns it. | [optional] 
**error** | **str** | Why the download failed. Present when &#x60;status&#x60; is &#x60;failed&#x60;. | [optional] 
**download_id** | **str** | Present when &#x60;status&#x60; is &#x60;pending&#x60;. Pass it to &#x60;getRemoteUploadStatus&#x60;. | [optional] 

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


