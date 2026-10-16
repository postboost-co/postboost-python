# FreeToolCalculateAspectRatioRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**width** | **int** | Width in pixels. | [optional] 
**height** | **int** | Height in pixels. | [optional] 
**ratio** | **str** | Ratio as width:height, e.g. &#x60;16:9&#x60; or &#x60;1.91:1&#x60;. Give it with width or height to get the other side. | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_aspect_ratio_request import FreeToolCalculateAspectRatioRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateAspectRatioRequest from a JSON string
free_tool_calculate_aspect_ratio_request_instance = FreeToolCalculateAspectRatioRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateAspectRatioRequest.to_json())

# convert the object into a dict
free_tool_calculate_aspect_ratio_request_dict = free_tool_calculate_aspect_ratio_request_instance.to_dict()
# create an instance of FreeToolCalculateAspectRatioRequest from a dict
free_tool_calculate_aspect_ratio_request_from_dict = FreeToolCalculateAspectRatioRequest.from_dict(free_tool_calculate_aspect_ratio_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


