# FreeToolPlanPostingFrequencyResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**posts_per_week_capacity** | **int** |  | [optional] 
**sum_of_minimums** | **int** | The recommended minimums of the chosen networks added up. | [optional] 
**networks** | [**List[FreeToolPlanPostingFrequencyResponseNetworksInner]**](FreeToolPlanPostingFrequencyResponseNetworksInner.md) | One row per chosen network, in a fixed network order. | [optional] 
**slots** | [**List[FreeToolPlanPostingFrequencyResponseSlotsInner]**](FreeToolPlanPostingFrequencyResponseSlotsInner.md) | The weekly grid: each network&#39;s posts spread evenly from Monday, sorted by day. | [optional] 
**warnings** | **List[str]** |  | [optional] 
**last_verified** | **date** | When the ranges were last checked against their sources. | [optional] 

## Example

```python
from postboost.models.free_tool_plan_posting_frequency_response import FreeToolPlanPostingFrequencyResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPlanPostingFrequencyResponse from a JSON string
free_tool_plan_posting_frequency_response_instance = FreeToolPlanPostingFrequencyResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolPlanPostingFrequencyResponse.to_json())

# convert the object into a dict
free_tool_plan_posting_frequency_response_dict = free_tool_plan_posting_frequency_response_instance.to_dict()
# create an instance of FreeToolPlanPostingFrequencyResponse from a dict
free_tool_plan_posting_frequency_response_from_dict = FreeToolPlanPostingFrequencyResponse.from_dict(free_tool_plan_posting_frequency_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


