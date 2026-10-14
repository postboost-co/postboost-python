# FreeToolCalculateEngagementRateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**engagements** | **int** |  | [optional] 
**posts** | **int** |  | [optional] 
**rate** | **float** | Percent, 2 decimals. | [optional] 
**formula** | **str** |  | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_engagement_rate_response import FreeToolCalculateEngagementRateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateEngagementRateResponse from a JSON string
free_tool_calculate_engagement_rate_response_instance = FreeToolCalculateEngagementRateResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateEngagementRateResponse.to_json())

# convert the object into a dict
free_tool_calculate_engagement_rate_response_dict = free_tool_calculate_engagement_rate_response_instance.to_dict()
# create an instance of FreeToolCalculateEngagementRateResponse from a dict
free_tool_calculate_engagement_rate_response_from_dict = FreeToolCalculateEngagementRateResponse.from_dict(free_tool_calculate_engagement_rate_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


