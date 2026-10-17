# FreeToolPlanPostingFrequencyRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**networks** | **List[str]** | The networks you post on. Bluesky and Mastodon are not offered: no published frequency we could verify. | 
**posts_per_week_capacity** | **int** | How many posts your team can make in a week, across all networks. | 

## Example

```python
from postboost.models.free_tool_plan_posting_frequency_request import FreeToolPlanPostingFrequencyRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPlanPostingFrequencyRequest from a JSON string
free_tool_plan_posting_frequency_request_instance = FreeToolPlanPostingFrequencyRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolPlanPostingFrequencyRequest.to_json())

# convert the object into a dict
free_tool_plan_posting_frequency_request_dict = free_tool_plan_posting_frequency_request_instance.to_dict()
# create an instance of FreeToolPlanPostingFrequencyRequest from a dict
free_tool_plan_posting_frequency_request_from_dict = FreeToolPlanPostingFrequencyRequest.from_dict(free_tool_plan_posting_frequency_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


