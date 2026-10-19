# FreeToolCalculateSmmPricingResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **str** |  | [optional] 
**pricing_model** | **str** |  | [optional] 
**posts_per_month** | **float** | Networks × posts per week × 52 ÷ 12, 1 decimal. | [optional] 
**hours_per_month** | **float** | Estimated working hours a month, 1 decimal. | [optional] 
**hourly_rate** | **float** |  | [optional] 
**monthly_retainer** | **float** | Hours a month × hourly rate, whole currency units. | [optional] 
**per_post** | **float** | Monthly retainer ÷ posts a month, 2 decimals; null with no posts. | [optional] 
**range** | [**FreeToolCalculateSmmPricingResponseRange**](FreeToolCalculateSmmPricingResponseRange.md) |  | [optional] 
**line_items** | [**List[FreeToolCalculateSmmPricingResponseLineItemsInner]**](FreeToolCalculateSmmPricingResponseLineItemsInner.md) | Every task with hours above 0. | [optional] 
**assumptions** | **List[str]** |  | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_smm_pricing_response import FreeToolCalculateSmmPricingResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateSmmPricingResponse from a JSON string
free_tool_calculate_smm_pricing_response_instance = FreeToolCalculateSmmPricingResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateSmmPricingResponse.to_json())

# convert the object into a dict
free_tool_calculate_smm_pricing_response_dict = free_tool_calculate_smm_pricing_response_instance.to_dict()
# create an instance of FreeToolCalculateSmmPricingResponse from a dict
free_tool_calculate_smm_pricing_response_from_dict = FreeToolCalculateSmmPricingResponse.from_dict(free_tool_calculate_smm_pricing_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


