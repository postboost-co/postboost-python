# FreeToolCalculateCropRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**width** | **int** | Source image width in pixels. | 
**height** | **int** | Source image height in pixels. | 
**network** | **str** | Network key from getImageSizes (&#x60;network_key&#x60;), e.g. &#x60;instagram&#x60;. With &#x60;format&#x60;, picks the target size. | [optional] 
**format** | **str** | Format key from getImageSizes (&#x60;format_key&#x60;), e.g. &#x60;feed-square&#x60;. | [optional] 
**target_width** | **int** | Target width in pixels, instead of &#x60;network&#x60; + &#x60;format&#x60;. | [optional] 
**target_height** | **int** | Target height in pixels, instead of &#x60;network&#x60; + &#x60;format&#x60;. | [optional] 
**fit** | **str** | &#x60;cover&#x60; crops to fill the target; &#x60;contain&#x60; keeps the whole image and centres it. | [optional] [default to 'cover']

## Example

```python
from postboost.models.free_tool_calculate_crop_request import FreeToolCalculateCropRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateCropRequest from a JSON string
free_tool_calculate_crop_request_instance = FreeToolCalculateCropRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateCropRequest.to_json())

# convert the object into a dict
free_tool_calculate_crop_request_dict = free_tool_calculate_crop_request_instance.to_dict()
# create an instance of FreeToolCalculateCropRequest from a dict
free_tool_calculate_crop_request_from_dict = FreeToolCalculateCropRequest.from_dict(free_tool_calculate_crop_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


