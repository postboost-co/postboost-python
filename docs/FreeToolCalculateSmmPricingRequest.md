# FreeToolCalculateSmmPricingRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**networks** | **int** | Number of social networks managed. | 
**posts_per_week** | **int** | Posts per week on each network. | 
**content_type** | **str** | What goes into a post. Assumed minutes per post: copy 30, copy_design 60, copy_design_video 120. | [optional] [default to 'copy_design']
**community_hours_per_week** | **float** | Community management (replies, comments, DMs), hours per week. | [optional] [default to 0]
**reporting_hours_per_month** | **float** | Reporting, hours per month. | [optional] [default to 0]
**ad_hours_per_month** | **float** | Paid social ad management, hours per month. | [optional] [default to 0]
**hourly_rate** | **float** | Your hourly rate. The default 50 is a round placeholder, not a market rate. | [optional] [default to 50]
**currency** | **str** | Currency for formatting only; nothing is converted. | [optional] [default to 'USD']
**pricing_model** | **str** | Which price leads the quote: hourly, monthly retainer or per post. | [optional] [default to 'retainer']

## Example

```python
from postboost.models.free_tool_calculate_smm_pricing_request import FreeToolCalculateSmmPricingRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateSmmPricingRequest from a JSON string
free_tool_calculate_smm_pricing_request_instance = FreeToolCalculateSmmPricingRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateSmmPricingRequest.to_json())

# convert the object into a dict
free_tool_calculate_smm_pricing_request_dict = free_tool_calculate_smm_pricing_request_instance.to_dict()
# create an instance of FreeToolCalculateSmmPricingRequest from a dict
free_tool_calculate_smm_pricing_request_from_dict = FreeToolCalculateSmmPricingRequest.from_dict(free_tool_calculate_smm_pricing_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


