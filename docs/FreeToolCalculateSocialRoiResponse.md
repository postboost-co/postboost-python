# FreeToolCalculateSocialRoiResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **str** |  | [optional] 
**revenue** | **float** |  | [optional] 
**total_cost** | **float** | Sum of every cost, labor &#x3D; hours × hourly rate. 2 decimals. | [optional] 
**net_return** | **float** | Revenue minus total cost. 2 decimals. | [optional] 
**roi_percent** | **float** | (revenue − total cost) ÷ total cost × 100, 1 decimal; null when the total cost is 0. | [optional] 
**cost_breakdown** | [**List[FreeToolCalculateSocialRoiResponseCostBreakdownInner]**](FreeToolCalculateSocialRoiResponseCostBreakdownInner.md) | Every cost above 0, with its share of the total cost (percent, 1 decimal). | [optional] 
**warnings** | **List[str]** |  | [optional] 
**formula** | **str** |  | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_social_roi_response import FreeToolCalculateSocialRoiResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateSocialRoiResponse from a JSON string
free_tool_calculate_social_roi_response_instance = FreeToolCalculateSocialRoiResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateSocialRoiResponse.to_json())

# convert the object into a dict
free_tool_calculate_social_roi_response_dict = free_tool_calculate_social_roi_response_instance.to_dict()
# create an instance of FreeToolCalculateSocialRoiResponse from a dict
free_tool_calculate_social_roi_response_from_dict = FreeToolCalculateSocialRoiResponse.from_dict(free_tool_calculate_social_roi_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


