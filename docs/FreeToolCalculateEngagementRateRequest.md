# FreeToolCalculateEngagementRateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**likes** | **int** |  | [optional] [default to 0]
**comments** | **int** |  | [optional] [default to 0]
**shares** | **int** |  | [optional] [default to 0]
**saves** | **int** |  | [optional] [default to 0]
**clicks** | **int** |  | [optional] [default to 0]
**method** | **str** | What to divide by. | [optional] [default to 'followers']
**base** | **int** | Followers, or the total reach or impressions of the posts. | 
**posts** | **int** | Number of posts the engagements come from. | [optional] [default to 1]

## Example

```python
from postboost.models.free_tool_calculate_engagement_rate_request import FreeToolCalculateEngagementRateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateEngagementRateRequest from a JSON string
free_tool_calculate_engagement_rate_request_instance = FreeToolCalculateEngagementRateRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateEngagementRateRequest.to_json())

# convert the object into a dict
free_tool_calculate_engagement_rate_request_dict = free_tool_calculate_engagement_rate_request_instance.to_dict()
# create an instance of FreeToolCalculateEngagementRateRequest from a dict
free_tool_calculate_engagement_rate_request_from_dict = FreeToolCalculateEngagementRateRequest.from_dict(free_tool_calculate_engagement_rate_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


