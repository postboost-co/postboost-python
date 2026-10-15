# FreeToolGetBestTimesToPostResponseNetworksInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**network** | **str** |  | [optional] 
**network_key** | **str** | Key for &#x60;network&#x60;. | [optional] 
**columns** | **List[str]** | One column per study. | [optional] 
**rows** | **List[List[str]]** | Weekday (or &#x60;Best&#x60;), then one cell per study, in the audience&#39;s local time. | [optional] 

## Example

```python
from postboost.models.free_tool_get_best_times_to_post_response_networks_inner import FreeToolGetBestTimesToPostResponseNetworksInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetBestTimesToPostResponseNetworksInner from a JSON string
free_tool_get_best_times_to_post_response_networks_inner_instance = FreeToolGetBestTimesToPostResponseNetworksInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetBestTimesToPostResponseNetworksInner.to_json())

# convert the object into a dict
free_tool_get_best_times_to_post_response_networks_inner_dict = free_tool_get_best_times_to_post_response_networks_inner_instance.to_dict()
# create an instance of FreeToolGetBestTimesToPostResponseNetworksInner from a dict
free_tool_get_best_times_to_post_response_networks_inner_from_dict = FreeToolGetBestTimesToPostResponseNetworksInner.from_dict(free_tool_get_best_times_to_post_response_networks_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


