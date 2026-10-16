# FreeToolCalculateXApiCostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**posts** | **int** | Posts created per month, with or without a link. | [optional] [default to 0]
**link_share** | **int** | Percent of those posts that contain a URL (billed at the link-post price). | [optional] [default to 0]
**replies** | **int** | Summoned replies per month. | [optional] [default to 0]
**post_reads** | **int** | Posts read per month. | [optional] [default to 0]
**user_reads** | **int** | Users read per month. | [optional] [default to 0]
**owned_reads** | **int** | Owned resources read per month (your own posts, followers and so on). | [optional] [default to 0]

## Example

```python
from postboost.models.free_tool_calculate_x_api_cost_request import FreeToolCalculateXApiCostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateXApiCostRequest from a JSON string
free_tool_calculate_x_api_cost_request_instance = FreeToolCalculateXApiCostRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateXApiCostRequest.to_json())

# convert the object into a dict
free_tool_calculate_x_api_cost_request_dict = free_tool_calculate_x_api_cost_request_instance.to_dict()
# create an instance of FreeToolCalculateXApiCostRequest from a dict
free_tool_calculate_x_api_cost_request_from_dict = FreeToolCalculateXApiCostRequest.from_dict(free_tool_calculate_x_api_cost_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


