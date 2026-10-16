# FreeToolCalculateSocialRoiRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**revenue** | **float** | Revenue attributed to social media in the period, in USD. | 
**costs** | [**FreeToolCalculateSocialRoiRequestCosts**](FreeToolCalculateSocialRoiRequestCosts.md) |  | [optional] 
**period** | **str** | Optional label for the period, e.g. \&quot;Q3 2026\&quot;. | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_social_roi_request import FreeToolCalculateSocialRoiRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateSocialRoiRequest from a JSON string
free_tool_calculate_social_roi_request_instance = FreeToolCalculateSocialRoiRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateSocialRoiRequest.to_json())

# convert the object into a dict
free_tool_calculate_social_roi_request_dict = free_tool_calculate_social_roi_request_instance.to_dict()
# create an instance of FreeToolCalculateSocialRoiRequest from a dict
free_tool_calculate_social_roi_request_from_dict = FreeToolCalculateSocialRoiRequest.from_dict(free_tool_calculate_social_roi_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


