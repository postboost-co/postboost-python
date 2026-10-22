# FreeToolGenerateSocialPostsFromVideoResponseOutputs

One entry per requested output that came back usable.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**x_thread** | **List[str]** | The thread&#39;s posts in order, each within X&#39;s 280 weighted characters; the link is in the last one. | [optional] 
**linkedin** | **str** | A LinkedIn caption within the network&#39;s character limit. | [optional] 
**instagram** | **str** | A Instagram caption within the network&#39;s character limit. | [optional] 
**facebook** | **str** | A Facebook caption within the network&#39;s character limit. | [optional] 
**threads** | **str** | A Threads caption within the network&#39;s character limit. | [optional] 
**bluesky** | **str** | A Bluesky caption within the network&#39;s character limit. | [optional] 
**mastodon** | **str** | A Mastodon caption within the network&#39;s character limit. | [optional] 

## Example

```python
from postboost.models.free_tool_generate_social_posts_from_video_response_outputs import FreeToolGenerateSocialPostsFromVideoResponseOutputs

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateSocialPostsFromVideoResponseOutputs from a JSON string
free_tool_generate_social_posts_from_video_response_outputs_instance = FreeToolGenerateSocialPostsFromVideoResponseOutputs.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateSocialPostsFromVideoResponseOutputs.to_json())

# convert the object into a dict
free_tool_generate_social_posts_from_video_response_outputs_dict = free_tool_generate_social_posts_from_video_response_outputs_instance.to_dict()
# create an instance of FreeToolGenerateSocialPostsFromVideoResponseOutputs from a dict
free_tool_generate_social_posts_from_video_response_outputs_from_dict = FreeToolGenerateSocialPostsFromVideoResponseOutputs.from_dict(free_tool_generate_social_posts_from_video_response_outputs_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


