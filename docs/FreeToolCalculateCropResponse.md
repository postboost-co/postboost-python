# FreeToolCalculateCropResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**crop** | [**FreeToolCalculateCropResponseCrop**](FreeToolCalculateCropResponseCrop.md) |  | [optional] 
**output** | [**FreeToolCalculateCropResponseOutput**](FreeToolCalculateCropResponseOutput.md) |  | [optional] 
**image** | [**FreeToolCalculateCropResponseImage**](FreeToolCalculateCropResponseImage.md) |  | [optional] 
**scale** | **float** | Output pixels per source pixel, 4 decimals. | [optional] 
**upscaled** | **bool** | True when the source is enlarged (scale above 1), which can look soft. | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_crop_response import FreeToolCalculateCropResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateCropResponse from a JSON string
free_tool_calculate_crop_response_instance = FreeToolCalculateCropResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateCropResponse.to_json())

# convert the object into a dict
free_tool_calculate_crop_response_dict = free_tool_calculate_crop_response_instance.to_dict()
# create an instance of FreeToolCalculateCropResponse from a dict
free_tool_calculate_crop_response_from_dict = FreeToolCalculateCropResponse.from_dict(free_tool_calculate_crop_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


