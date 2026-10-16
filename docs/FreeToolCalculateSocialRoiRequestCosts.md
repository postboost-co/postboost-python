# FreeToolCalculateSocialRoiRequestCosts

What social media cost in the period, in USD. Every field is optional.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_spend** | **float** | Paid social ad spend. | [optional] [default to 0]
**tools** | **float** | Tools and software subscriptions. | [optional] [default to 0]
**labor_hours** | **float** | Hours spent on social media. | [optional] [default to 0]
**hourly_rate** | **float** | Cost of one hour of that work. | [optional] [default to 0]
**content** | **float** | Content production: design, video, photography, freelancers. | [optional] [default to 0]
**other** | **float** | Anything else. | [optional] [default to 0]

## Example

```python
from postboost.models.free_tool_calculate_social_roi_request_costs import FreeToolCalculateSocialRoiRequestCosts

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateSocialRoiRequestCosts from a JSON string
free_tool_calculate_social_roi_request_costs_instance = FreeToolCalculateSocialRoiRequestCosts.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateSocialRoiRequestCosts.to_json())

# convert the object into a dict
free_tool_calculate_social_roi_request_costs_dict = free_tool_calculate_social_roi_request_costs_instance.to_dict()
# create an instance of FreeToolCalculateSocialRoiRequestCosts from a dict
free_tool_calculate_social_roi_request_costs_from_dict = FreeToolCalculateSocialRoiRequestCosts.from_dict(free_tool_calculate_social_roi_request_costs_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


