# FreeToolCalculateCarouselSlicesRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**width** | **int** | Source image width in pixels. | 
**height** | **int** | Source image height in pixels. | 
**slides** | **int** | Number of carousel slides, 2 to 10 (the most a carousel published through the Instagram API can hold). | 
**ratio** | **str** | Shape of each slide: &#x60;1:1&#x60; (1080 × 1080) or &#x60;4:5&#x60; (1080 × 1350). | [optional] [default to '4:5']

## Example

```python
from postboost.models.free_tool_calculate_carousel_slices_request import FreeToolCalculateCarouselSlicesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateCarouselSlicesRequest from a JSON string
free_tool_calculate_carousel_slices_request_instance = FreeToolCalculateCarouselSlicesRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateCarouselSlicesRequest.to_json())

# convert the object into a dict
free_tool_calculate_carousel_slices_request_dict = free_tool_calculate_carousel_slices_request_instance.to_dict()
# create an instance of FreeToolCalculateCarouselSlicesRequest from a dict
free_tool_calculate_carousel_slices_request_from_dict = FreeToolCalculateCarouselSlicesRequest.from_dict(free_tool_calculate_carousel_slices_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


