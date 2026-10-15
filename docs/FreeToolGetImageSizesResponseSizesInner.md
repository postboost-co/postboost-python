# FreeToolGetImageSizesResponseSizesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**network** | **str** | Network name. | [optional] 
**network_key** | **str** | Key for &#x60;network&#x60; here and in calculateCrop. | [optional] 
**placement** | **str** | Where the image appears. | [optional] 
**format_key** | **str** | Key for &#x60;format&#x60; in calculateCrop. | [optional] 
**size** | **str** | The size as the network states it, ranges included. | [optional] 
**width** | **int** | Recommended width in pixels, when the size is one fixed size. | [optional] 
**height** | **int** | Recommended height in pixels, when the size is one fixed size. | [optional] 
**ratio** | **str** | Aspect ratio. | [optional] 
**limits** | **str** | File type and size limits. | [optional] 
**basis** | **str** | &#x60;official&#x60; when the network itself states it, else how it was found. | [optional] 
**source** | **str** | URL of the source. | [optional] 

## Example

```python
from postboost.models.free_tool_get_image_sizes_response_sizes_inner import FreeToolGetImageSizesResponseSizesInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetImageSizesResponseSizesInner from a JSON string
free_tool_get_image_sizes_response_sizes_inner_instance = FreeToolGetImageSizesResponseSizesInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetImageSizesResponseSizesInner.to_json())

# convert the object into a dict
free_tool_get_image_sizes_response_sizes_inner_dict = free_tool_get_image_sizes_response_sizes_inner_instance.to_dict()
# create an instance of FreeToolGetImageSizesResponseSizesInner from a dict
free_tool_get_image_sizes_response_sizes_inner_from_dict = FreeToolGetImageSizesResponseSizesInner.from_dict(free_tool_get_image_sizes_response_sizes_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


