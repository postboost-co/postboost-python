# FreeToolFormatInstagramCaptionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**spacer** | **str** | What fills a blank line: braille (U+2800 Braille blank, shows as an empty line) or dot (a line with \&quot;.\&quot;). | [optional] [default to 'braille']
**hashtags_to_end** | **bool** | Move the hashtags that end a line to the bottom, after three spacer lines. A hashtag inside a sentence stays where it is. | [optional] [default to False]

## Example

```python
from postboost.models.free_tool_format_instagram_caption_request import FreeToolFormatInstagramCaptionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolFormatInstagramCaptionRequest from a JSON string
free_tool_format_instagram_caption_request_instance = FreeToolFormatInstagramCaptionRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolFormatInstagramCaptionRequest.to_json())

# convert the object into a dict
free_tool_format_instagram_caption_request_dict = free_tool_format_instagram_caption_request_instance.to_dict()
# create an instance of FreeToolFormatInstagramCaptionRequest from a dict
free_tool_format_instagram_caption_request_from_dict = FreeToolFormatInstagramCaptionRequest.from_dict(free_tool_format_instagram_caption_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


