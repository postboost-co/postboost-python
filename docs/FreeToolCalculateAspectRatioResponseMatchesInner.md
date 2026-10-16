# FreeToolCalculateAspectRatioResponseMatchesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**network** | **str** | Network key from getImageSizes (&#x60;network_key&#x60;). | [optional] 
**format** | **str** | Format key from getImageSizes (&#x60;format_key&#x60;). | [optional] 
**width** | **int** |  | [optional] 
**height** | **int** |  | [optional] 
**ratio** | **str** |  | [optional] 
**exact** | **bool** | False when no preset has the same ratio and these are the nearest. | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_aspect_ratio_response_matches_inner import FreeToolCalculateAspectRatioResponseMatchesInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateAspectRatioResponseMatchesInner from a JSON string
free_tool_calculate_aspect_ratio_response_matches_inner_instance = FreeToolCalculateAspectRatioResponseMatchesInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateAspectRatioResponseMatchesInner.to_json())

# convert the object into a dict
free_tool_calculate_aspect_ratio_response_matches_inner_dict = free_tool_calculate_aspect_ratio_response_matches_inner_instance.to_dict()
# create an instance of FreeToolCalculateAspectRatioResponseMatchesInner from a dict
free_tool_calculate_aspect_ratio_response_matches_inner_from_dict = FreeToolCalculateAspectRatioResponseMatchesInner.from_dict(free_tool_calculate_aspect_ratio_response_matches_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


