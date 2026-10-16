# FreeToolGetVideoSpecsResponseSpecsInnerLimits

The row as numbers, for checking a video.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**min_seconds** | **float** | Shortest length. Null when the source states no figure. | [optional] 
**max_seconds** | **float** | Longest length. Null when the source states no figure. | [optional] 
**warn_over_seconds** | **float** | Longer videos need a check (account type, reach), see &#x60;length&#x60;. Null when the source states no figure. | [optional] 
**min_ratio** | **float** | Narrowest width / height. Null when the source states no figure. | [optional] 
**max_ratio** | **float** | Widest width / height. Null when the source states no figure. | [optional] 
**recommended_ratio** | **str** | Recommended ratio, e.g. &#x60;9:16&#x60;. | [optional] 
**max_mb** | **float** | Largest file in MB. Null when the source states no figure. | [optional] 

## Example

```python
from postboost.models.free_tool_get_video_specs_response_specs_inner_limits import FreeToolGetVideoSpecsResponseSpecsInnerLimits

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetVideoSpecsResponseSpecsInnerLimits from a JSON string
free_tool_get_video_specs_response_specs_inner_limits_instance = FreeToolGetVideoSpecsResponseSpecsInnerLimits.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetVideoSpecsResponseSpecsInnerLimits.to_json())

# convert the object into a dict
free_tool_get_video_specs_response_specs_inner_limits_dict = free_tool_get_video_specs_response_specs_inner_limits_instance.to_dict()
# create an instance of FreeToolGetVideoSpecsResponseSpecsInnerLimits from a dict
free_tool_get_video_specs_response_specs_inner_limits_from_dict = FreeToolGetVideoSpecsResponseSpecsInnerLimits.from_dict(free_tool_get_video_specs_response_specs_inner_limits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


