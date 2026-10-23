# FreeToolGenerateYoutubeTitlesRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | What the video is about. | 
**style** | **str** | how-to (\&quot;How to ...\&quot;), listicle (\&quot;7 ways to ...\&quot;), question, story (first person) or news. | [optional] [default to 'how-to']
**workspace** | **str** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] 
**transcript** | **str** | Optional: your video&#39;s captions (.srt, .vtt, .sbv or the Show transcript text) as context; timestamps are removed and the first 6,000 characters are used. | [optional] 

## Example

```python
from postboost.models.free_tool_generate_youtube_titles_request import FreeToolGenerateYoutubeTitlesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateYoutubeTitlesRequest from a JSON string
free_tool_generate_youtube_titles_request_instance = FreeToolGenerateYoutubeTitlesRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateYoutubeTitlesRequest.to_json())

# convert the object into a dict
free_tool_generate_youtube_titles_request_dict = free_tool_generate_youtube_titles_request_instance.to_dict()
# create an instance of FreeToolGenerateYoutubeTitlesRequest from a dict
free_tool_generate_youtube_titles_request_from_dict = FreeToolGenerateYoutubeTitlesRequest.from_dict(free_tool_generate_youtube_titles_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


