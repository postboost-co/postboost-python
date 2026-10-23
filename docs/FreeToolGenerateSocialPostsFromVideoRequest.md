# FreeToolGenerateSocialPostsFromVideoRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | The captions of your video: an .srt, .vtt or .sbv file&#39;s text, or the text of YouTube&#39;s \&quot;Show transcript\&quot; panel. Timestamps, cue numbers and sound tags like [Music] are removed; 100 to 24,000 characters must remain. | 
**video_url** | **str** | The video&#39;s YouTube link (watch, youtu.be, Shorts or live). Each output links it once, the X thread in its last post; without it the posts have no link. | [optional] 
**title** | **str** | The video&#39;s title, as context for the posts. | [optional] 
**outputs** | **List[str]** | What to write, 1 to 4 different keys. | [optional] [default to [x_thread, linkedin, instagram]]
**tone** | **str** |  | [optional] [default to 'friendly']
**workspace** | **str** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_social_posts_from_video_request import FreeToolGenerateSocialPostsFromVideoRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateSocialPostsFromVideoRequest from a JSON string
free_tool_generate_social_posts_from_video_request_instance = FreeToolGenerateSocialPostsFromVideoRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateSocialPostsFromVideoRequest.to_json())

# convert the object into a dict
free_tool_generate_social_posts_from_video_request_dict = free_tool_generate_social_posts_from_video_request_instance.to_dict()
# create an instance of FreeToolGenerateSocialPostsFromVideoRequest from a dict
free_tool_generate_social_posts_from_video_request_from_dict = FreeToolGenerateSocialPostsFromVideoRequest.from_dict(free_tool_generate_social_posts_from_video_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


