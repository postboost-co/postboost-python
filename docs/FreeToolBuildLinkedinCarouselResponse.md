# FreeToolBuildLinkedinCarouselResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | [**FreeToolBuildLinkedinCarouselResponsePage**](FreeToolBuildLinkedinCarouselResponsePage.md) |  | [optional] 
**slides** | [**List[FreeToolBuildLinkedinCarouselResponseSlidesInner]**](FreeToolBuildLinkedinCarouselResponseSlidesInner.md) |  | [optional] 
**warnings** | [**List[FreeToolBuildLinkedinCarouselResponseWarningsInner]**](FreeToolBuildLinkedinCarouselResponseWarningsInner.md) |  | [optional] 
**limits** | [**FreeToolBuildLinkedinCarouselResponseLimits**](FreeToolBuildLinkedinCarouselResponseLimits.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_build_linkedin_carousel_response import FreeToolBuildLinkedinCarouselResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolBuildLinkedinCarouselResponse from a JSON string
free_tool_build_linkedin_carousel_response_instance = FreeToolBuildLinkedinCarouselResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolBuildLinkedinCarouselResponse.to_json())

# convert the object into a dict
free_tool_build_linkedin_carousel_response_dict = free_tool_build_linkedin_carousel_response_instance.to_dict()
# create an instance of FreeToolBuildLinkedinCarouselResponse from a dict
free_tool_build_linkedin_carousel_response_from_dict = FreeToolBuildLinkedinCarouselResponse.from_dict(free_tool_build_linkedin_carousel_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


