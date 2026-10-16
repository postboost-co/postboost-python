# FreeToolCalculateAspectRatioResponseRounding

Set when the calculated side is not a whole number: which side, its exact value (2 decimals) and the rounded pixels returned.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**side** | **str** |  | [optional] 
**exact** | **float** |  | [optional] 
**rounded** | **int** |  | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_aspect_ratio_response_rounding import FreeToolCalculateAspectRatioResponseRounding

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateAspectRatioResponseRounding from a JSON string
free_tool_calculate_aspect_ratio_response_rounding_instance = FreeToolCalculateAspectRatioResponseRounding.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateAspectRatioResponseRounding.to_json())

# convert the object into a dict
free_tool_calculate_aspect_ratio_response_rounding_dict = free_tool_calculate_aspect_ratio_response_rounding_instance.to_dict()
# create an instance of FreeToolCalculateAspectRatioResponseRounding from a dict
free_tool_calculate_aspect_ratio_response_rounding_from_dict = FreeToolCalculateAspectRatioResponseRounding.from_dict(free_tool_calculate_aspect_ratio_response_rounding_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


