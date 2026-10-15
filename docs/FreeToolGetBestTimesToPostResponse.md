# FreeToolGetBestTimesToPostResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**networks** | [**List[FreeToolGetBestTimesToPostResponseNetworksInner]**](FreeToolGetBestTimesToPostResponseNetworksInner.md) |  | [optional] 
**last_verified** | **date** | When the data was last checked against its sources. | [optional] 
**sources** | [**List[FreeToolGetImageSizesResponseSourcesInner]**](FreeToolGetImageSizesResponseSourcesInner.md) | Sources of the whole dataset (rows may name their own). | [optional] 
**per_account** | **str** | Where to get times from your own accounts. | [optional] 

## Example

```python
from postboost.models.free_tool_get_best_times_to_post_response import FreeToolGetBestTimesToPostResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetBestTimesToPostResponse from a JSON string
free_tool_get_best_times_to_post_response_instance = FreeToolGetBestTimesToPostResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetBestTimesToPostResponse.to_json())

# convert the object into a dict
free_tool_get_best_times_to_post_response_dict = free_tool_get_best_times_to_post_response_instance.to_dict()
# create an instance of FreeToolGetBestTimesToPostResponse from a dict
free_tool_get_best_times_to_post_response_from_dict = FreeToolGetBestTimesToPostResponse.from_dict(free_tool_get_best_times_to_post_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


