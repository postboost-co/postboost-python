# FreeToolBuildLinkedinCarouselResponseSlidesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**n** | **int** | Slide number, 1 to N. | [optional] 
**kind** | **str** |  | [optional] 
**heading** | **str** |  | [optional] 
**body** | **List[str]** | Lines; bullets start with \&quot;• \&quot;, numbered lines keep their number. | [optional] 

## Example

```python
from postboost.models.free_tool_build_linkedin_carousel_response_slides_inner import FreeToolBuildLinkedinCarouselResponseSlidesInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolBuildLinkedinCarouselResponseSlidesInner from a JSON string
free_tool_build_linkedin_carousel_response_slides_inner_instance = FreeToolBuildLinkedinCarouselResponseSlidesInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolBuildLinkedinCarouselResponseSlidesInner.to_json())

# convert the object into a dict
free_tool_build_linkedin_carousel_response_slides_inner_dict = free_tool_build_linkedin_carousel_response_slides_inner_instance.to_dict()
# create an instance of FreeToolBuildLinkedinCarouselResponseSlidesInner from a dict
free_tool_build_linkedin_carousel_response_slides_inner_from_dict = FreeToolBuildLinkedinCarouselResponseSlidesInner.from_dict(free_tool_build_linkedin_carousel_response_slides_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


