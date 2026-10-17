# FreeToolPlanPostingFrequencyResponseNetworksInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**network** | **str** |  | [optional] 
**label** | **str** |  | [optional] 
**recommended_per_week** | [**FreeToolPlanPostingFrequencyResponseNetworksInnerRecommendedPerWeek**](FreeToolPlanPostingFrequencyResponseNetworksInnerRecommendedPerWeek.md) |  | [optional] 
**recommended_label** | **str** | The range as text, e.g. \&quot;3-5 per week\&quot; or \&quot;1+ per week\&quot;. | [optional] 
**allocated_per_week** | **int** | Your posts for this network: capacity split in proportion to the range midpoints (the minimum for an open-ended range). | [optional] 
**fit** | **str** | Where the allocation sits against the recommended range. | [optional] 
**source_type** | **str** | measured &#x3D; a study of real posts; vendor &#x3D; a software vendor&#39;s guidance; platform &#x3D; the network&#39;s own guidance. | [optional] 
**sources** | [**List[FreeToolPlanPostingFrequencyResponseNetworksInnerSourcesInner]**](FreeToolPlanPostingFrequencyResponseNetworksInnerSourcesInner.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_plan_posting_frequency_response_networks_inner import FreeToolPlanPostingFrequencyResponseNetworksInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPlanPostingFrequencyResponseNetworksInner from a JSON string
free_tool_plan_posting_frequency_response_networks_inner_instance = FreeToolPlanPostingFrequencyResponseNetworksInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolPlanPostingFrequencyResponseNetworksInner.to_json())

# convert the object into a dict
free_tool_plan_posting_frequency_response_networks_inner_dict = free_tool_plan_posting_frequency_response_networks_inner_instance.to_dict()
# create an instance of FreeToolPlanPostingFrequencyResponseNetworksInner from a dict
free_tool_plan_posting_frequency_response_networks_inner_from_dict = FreeToolPlanPostingFrequencyResponseNetworksInner.from_dict(free_tool_plan_posting_frequency_response_networks_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


