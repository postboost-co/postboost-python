# FreeToolGenerateYoutubeDescriptionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**descriptions** | **List[str]** | Two or three different descriptions, each under 5,000 UTF-8 bytes (YouTube&#39;s limit) and without &#x60;&lt;&#x60; or &#x60;&gt;&#x60;. Links are &#x60;[link]&#x60; placeholders. | [optional] 
**credits_spent** | **int** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] 
**cached** | **bool** | True when the same request was answered before (free). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_youtube_description_response import FreeToolGenerateYoutubeDescriptionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateYoutubeDescriptionResponse from a JSON string
free_tool_generate_youtube_description_response_instance = FreeToolGenerateYoutubeDescriptionResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateYoutubeDescriptionResponse.to_json())

# convert the object into a dict
free_tool_generate_youtube_description_response_dict = free_tool_generate_youtube_description_response_instance.to_dict()
# create an instance of FreeToolGenerateYoutubeDescriptionResponse from a dict
free_tool_generate_youtube_description_response_from_dict = FreeToolGenerateYoutubeDescriptionResponse.from_dict(free_tool_generate_youtube_description_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


