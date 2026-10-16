# FreeToolFormatInstagramCaptionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | The caption with spacer lines, ready to paste into Instagram. | [optional] 
**count** | **int** | Characters, counted like the PostBoost composer counts an Instagram caption. | [optional] 
**limit** | **int** | Instagram caption limit. | [optional] 
**over** | **bool** |  | [optional] 
**hashtags** | **int** | Hashtags in the caption. | [optional] 
**max_hashtags** | **int** | Hashtags PostBoost allows per Instagram post. | [optional] 

## Example

```python
from postboost.models.free_tool_format_instagram_caption_response import FreeToolFormatInstagramCaptionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolFormatInstagramCaptionResponse from a JSON string
free_tool_format_instagram_caption_response_instance = FreeToolFormatInstagramCaptionResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolFormatInstagramCaptionResponse.to_json())

# convert the object into a dict
free_tool_format_instagram_caption_response_dict = free_tool_format_instagram_caption_response_instance.to_dict()
# create an instance of FreeToolFormatInstagramCaptionResponse from a dict
free_tool_format_instagram_caption_response_from_dict = FreeToolFormatInstagramCaptionResponse.from_dict(free_tool_format_instagram_caption_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


