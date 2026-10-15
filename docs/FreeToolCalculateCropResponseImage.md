# FreeToolCalculateCropResponseImage

Where the kept part is drawn in the finished image (`contain` leaves a margin).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**x** | **int** |  | [optional] 
**y** | **int** |  | [optional] 
**width** | **int** |  | [optional] 
**height** | **int** |  | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_crop_response_image import FreeToolCalculateCropResponseImage

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateCropResponseImage from a JSON string
free_tool_calculate_crop_response_image_instance = FreeToolCalculateCropResponseImage.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateCropResponseImage.to_json())

# convert the object into a dict
free_tool_calculate_crop_response_image_dict = free_tool_calculate_crop_response_image_instance.to_dict()
# create an instance of FreeToolCalculateCropResponseImage from a dict
free_tool_calculate_crop_response_image_from_dict = FreeToolCalculateCropResponseImage.from_dict(free_tool_calculate_crop_response_image_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


