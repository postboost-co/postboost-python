# FreeToolCalculateAspectRatioResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ratio** | **str** | Simplified ratio, e.g. &#x60;4:5&#x60;. Decimal ratios stay as given. | [optional] 
**decimal** | **float** | Width divided by height, 4 decimals. | [optional] 
**width** | **int** |  | [optional] 
**height** | **int** |  | [optional] 
**rounding** | [**FreeToolCalculateAspectRatioResponseRounding**](FreeToolCalculateAspectRatioResponseRounding.md) |  | [optional] 
**orientation** | **str** |  | [optional] 
**matches** | [**List[FreeToolCalculateAspectRatioResponseMatchesInner]**](FreeToolCalculateAspectRatioResponseMatchesInner.md) | Social media image presets with the same ratio, else the nearest. | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_aspect_ratio_response import FreeToolCalculateAspectRatioResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateAspectRatioResponse from a JSON string
free_tool_calculate_aspect_ratio_response_instance = FreeToolCalculateAspectRatioResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateAspectRatioResponse.to_json())

# convert the object into a dict
free_tool_calculate_aspect_ratio_response_dict = free_tool_calculate_aspect_ratio_response_instance.to_dict()
# create an instance of FreeToolCalculateAspectRatioResponse from a dict
free_tool_calculate_aspect_ratio_response_from_dict = FreeToolCalculateAspectRatioResponse.from_dict(free_tool_calculate_aspect_ratio_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


