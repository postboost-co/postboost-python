# FreeToolCalculateXApiCostResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**line_items** | [**List[FreeToolCalculateXApiCostResponseLineItemsInner]**](FreeToolCalculateXApiCostResponseLineItemsInner.md) | One row per billed resource: count × unit price. | [optional] 
**total_usd** | **float** | Sum of every line item. | [optional] 
**link_premium_usd** | **float** | What the link posts cost on top of the plain post price. | [optional] 
**notes** | **List[str]** |  | [optional] 
**prices_last_verified** | **date** | When the prices were last checked against the source. | [optional] 
**source** | **str** |  | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_x_api_cost_response import FreeToolCalculateXApiCostResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateXApiCostResponse from a JSON string
free_tool_calculate_x_api_cost_response_instance = FreeToolCalculateXApiCostResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateXApiCostResponse.to_json())

# convert the object into a dict
free_tool_calculate_x_api_cost_response_dict = free_tool_calculate_x_api_cost_response_instance.to_dict()
# create an instance of FreeToolCalculateXApiCostResponse from a dict
free_tool_calculate_x_api_cost_response_from_dict = FreeToolCalculateXApiCostResponse.from_dict(free_tool_calculate_x_api_cost_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


