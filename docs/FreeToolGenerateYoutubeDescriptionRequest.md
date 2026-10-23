# FreeToolGenerateYoutubeDescriptionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | What the video is about: a summary or the main points. | 
**keywords** | **str** | Optional search keywords to use naturally, comma separated. | [optional] 
**chapters** | **bool** | Add a chapters block after the first paragraph. | [optional] [default to False]
**chapter_lines** | **List[str]** | Your chapters as &#x60;m:ss Title&#x60; lines, the first at 0:00. Used verbatim when &#x60;chapters&#x60; is true; without them the block has fill-in placeholders. Timestamps are never generated. | [optional] 
**cta** | **str** | The closing call to action: subscribe, link (a [link] placeholder) or none. | [optional] [default to 'subscribe']
**workspace** | **str** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] 
**transcript** | **str** | Optional: your video&#39;s captions (.srt, .vtt or the Show transcript text) as context; timestamps are removed and the first 6,000 characters are used. | [optional] 

## Example

```python
from postboost.models.free_tool_generate_youtube_description_request import FreeToolGenerateYoutubeDescriptionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateYoutubeDescriptionRequest from a JSON string
free_tool_generate_youtube_description_request_instance = FreeToolGenerateYoutubeDescriptionRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateYoutubeDescriptionRequest.to_json())

# convert the object into a dict
free_tool_generate_youtube_description_request_dict = free_tool_generate_youtube_description_request_instance.to_dict()
# create an instance of FreeToolGenerateYoutubeDescriptionRequest from a dict
free_tool_generate_youtube_description_request_from_dict = FreeToolGenerateYoutubeDescriptionRequest.from_dict(free_tool_generate_youtube_description_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


