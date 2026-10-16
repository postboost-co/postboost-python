# FreeToolCalculateXApiCostResponseLineItemsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | [optional] 
**label** | **str** |  | [optional] 
**count** | **int** |  | [optional] 
**unit_usd** | **float** |  | [optional] 
**cost_usd** | **float** |  | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_x_api_cost_response_line_items_inner import FreeToolCalculateXApiCostResponseLineItemsInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateXApiCostResponseLineItemsInner from a JSON string
free_tool_calculate_x_api_cost_response_line_items_inner_instance = FreeToolCalculateXApiCostResponseLineItemsInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateXApiCostResponseLineItemsInner.to_json())

# convert the object into a dict
free_tool_calculate_x_api_cost_response_line_items_inner_dict = free_tool_calculate_x_api_cost_response_line_items_inner_instance.to_dict()
# create an instance of FreeToolCalculateXApiCostResponseLineItemsInner from a dict
free_tool_calculate_x_api_cost_response_line_items_inner_from_dict = FreeToolCalculateXApiCostResponseLineItemsInner.from_dict(free_tool_calculate_x_api_cost_response_line_items_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


