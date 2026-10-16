# FreeToolGetVideoSpecsResponseSpecsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**network** | **str** | Network name. | [optional] 
**network_key** | **str** | Key for &#x60;network&#x60;. | [optional] 
**placement** | **str** | Placement; &#x60;(app)&#x60; and &#x60;(publishing API)&#x60; rows differ where the network says so. | [optional] 
**placement_key** | **str** | Key for &#x60;placement&#x60;. | [optional] 
**ratio** | **str** | Aspect ratios as the source states them. | [optional] 
**resolution** | **str** | Resolution, frame rate and codec notes. | [optional] 
**length** | **str** | Length limits. | [optional] 
**max_size** | **str** | File size limit. | [optional] 
**formats** | **str** | Container and codec formats. | [optional] 
**safe_zone** | **str** | Text safe zone, only where the network publishes one. | [optional] 
**basis** | **str** | &#x60;official&#x60; when the network itself states it, else how it was found. | [optional] 
**sources** | **List[str]** | URLs of the sources. | [optional] 
**limits** | [**FreeToolGetVideoSpecsResponseSpecsInnerLimits**](FreeToolGetVideoSpecsResponseSpecsInnerLimits.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_get_video_specs_response_specs_inner import FreeToolGetVideoSpecsResponseSpecsInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetVideoSpecsResponseSpecsInner from a JSON string
free_tool_get_video_specs_response_specs_inner_instance = FreeToolGetVideoSpecsResponseSpecsInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetVideoSpecsResponseSpecsInner.to_json())

# convert the object into a dict
free_tool_get_video_specs_response_specs_inner_dict = free_tool_get_video_specs_response_specs_inner_instance.to_dict()
# create an instance of FreeToolGetVideoSpecsResponseSpecsInner from a dict
free_tool_get_video_specs_response_specs_inner_from_dict = FreeToolGetVideoSpecsResponseSpecsInner.from_dict(free_tool_get_video_specs_response_specs_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


