# FreeToolCalculateCarouselSlicesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slides** | [**List[FreeToolCalculateCarouselSlicesResponseSlidesInner]**](FreeToolCalculateCarouselSlicesResponseSlidesInner.md) | The part of the source image each slide shows, left to right, in source pixels. | [optional] 
**output** | [**FreeToolCalculateCarouselSlicesResponseOutput**](FreeToolCalculateCarouselSlicesResponseOutput.md) |  | [optional] 
**scale** | **float** | Output pixels per source pixel, 4 decimals. | [optional] 
**upscaled** | **bool** | True when the source is enlarged (scale above 1), which can look soft. | [optional] 
**warnings** | **List[str]** | Upscaling and how much of the source is cropped away. | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_carousel_slices_response import FreeToolCalculateCarouselSlicesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateCarouselSlicesResponse from a JSON string
free_tool_calculate_carousel_slices_response_instance = FreeToolCalculateCarouselSlicesResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateCarouselSlicesResponse.to_json())

# convert the object into a dict
free_tool_calculate_carousel_slices_response_dict = free_tool_calculate_carousel_slices_response_instance.to_dict()
# create an instance of FreeToolCalculateCarouselSlicesResponse from a dict
free_tool_calculate_carousel_slices_response_from_dict = FreeToolCalculateCarouselSlicesResponse.from_dict(free_tool_calculate_carousel_slices_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


