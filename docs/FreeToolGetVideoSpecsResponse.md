# FreeToolGetVideoSpecsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**specs** | [**List[FreeToolGetVideoSpecsResponseSpecsInner]**](FreeToolGetVideoSpecsResponseSpecsInner.md) |  | [optional] 
**last_verified** | **date** | When the data was last checked against its sources. | [optional] 
**sources** | [**List[FreeToolGetImageSizesResponseSourcesInner]**](FreeToolGetImageSizesResponseSourcesInner.md) | Sources of the whole dataset (rows may name their own). | [optional] 

## Example

```python
from postboost.models.free_tool_get_video_specs_response import FreeToolGetVideoSpecsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetVideoSpecsResponse from a JSON string
free_tool_get_video_specs_response_instance = FreeToolGetVideoSpecsResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetVideoSpecsResponse.to_json())

# convert the object into a dict
free_tool_get_video_specs_response_dict = free_tool_get_video_specs_response_instance.to_dict()
# create an instance of FreeToolGetVideoSpecsResponse from a dict
free_tool_get_video_specs_response_from_dict = FreeToolGetVideoSpecsResponse.from_dict(free_tool_get_video_specs_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


