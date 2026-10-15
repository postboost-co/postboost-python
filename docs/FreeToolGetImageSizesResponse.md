# FreeToolGetImageSizesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sizes** | [**List[FreeToolGetImageSizesResponseSizesInner]**](FreeToolGetImageSizesResponseSizesInner.md) |  | [optional] 
**last_verified** | **date** | When the data was last checked against its sources. | [optional] 
**sources** | [**List[FreeToolGetImageSizesResponseSourcesInner]**](FreeToolGetImageSizesResponseSourcesInner.md) | Sources of the whole dataset (rows may name their own). | [optional] 

## Example

```python
from postboost.models.free_tool_get_image_sizes_response import FreeToolGetImageSizesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetImageSizesResponse from a JSON string
free_tool_get_image_sizes_response_instance = FreeToolGetImageSizesResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetImageSizesResponse.to_json())

# convert the object into a dict
free_tool_get_image_sizes_response_dict = free_tool_get_image_sizes_response_instance.to_dict()
# create an instance of FreeToolGetImageSizesResponse from a dict
free_tool_get_image_sizes_response_from_dict = FreeToolGetImageSizesResponse.from_dict(free_tool_get_image_sizes_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


