# FreeToolBuildLinkedinCarouselRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | The post or outline. Blank lines separate slides; a first line starting with # (or a short first line without closing punctuation that is not a list item) is the slide heading; - * • lines become bullets. | 
**max_slides** | **int** | Most slides to return, 3 to 20. The cover and the CTA slide are always kept. | [optional] [default to 10]
**size** | **str** | Slide shape: &#x60;4:5&#x60; (1080 × 1350) or &#x60;1:1&#x60; (1080 × 1080). Every page of a LinkedIn document has the same size. | [optional] [default to '4:5']
**cover** | **bool** | Start with a cover slide: the first heading, or the first line of the text. | [optional] [default to True]
**cta** | **str** | Text of a closing call-to-action slide. | [optional] 

## Example

```python
from postboost.models.free_tool_build_linkedin_carousel_request import FreeToolBuildLinkedinCarouselRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolBuildLinkedinCarouselRequest from a JSON string
free_tool_build_linkedin_carousel_request_instance = FreeToolBuildLinkedinCarouselRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolBuildLinkedinCarouselRequest.to_json())

# convert the object into a dict
free_tool_build_linkedin_carousel_request_dict = free_tool_build_linkedin_carousel_request_instance.to_dict()
# create an instance of FreeToolBuildLinkedinCarouselRequest from a dict
free_tool_build_linkedin_carousel_request_from_dict = FreeToolBuildLinkedinCarouselRequest.from_dict(free_tool_build_linkedin_carousel_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


