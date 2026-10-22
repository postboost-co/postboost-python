# FreeToolGenerateSocialPostsFromVideoResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**outputs** | [**FreeToolGenerateSocialPostsFromVideoResponseOutputs**](FreeToolGenerateSocialPostsFromVideoResponseOutputs.md) |  | [optional] 
**outputs_skipped** | **List[str]** | Requested outputs that came back empty: generate again to get them. | [optional] 
**warnings** | **List[str]** | What to know before posting, in plain words. | [optional] 
**video_url** | **str** | The normalised video link the posts use, or null. | [optional] 
**cleaned_chars** | **int** | Characters of caption text left after cleaning; the model read these. | [optional] 
**removed_timestamps** | **bool** | True when timestamps, cue numbers, tags or repeated caption lines were removed. | [optional] 
**credits_spent** | **int** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] 
**cached** | **bool** | True when the same request was answered before (free). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_social_posts_from_video_response import FreeToolGenerateSocialPostsFromVideoResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateSocialPostsFromVideoResponse from a JSON string
free_tool_generate_social_posts_from_video_response_instance = FreeToolGenerateSocialPostsFromVideoResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateSocialPostsFromVideoResponse.to_json())

# convert the object into a dict
free_tool_generate_social_posts_from_video_response_dict = free_tool_generate_social_posts_from_video_response_instance.to_dict()
# create an instance of FreeToolGenerateSocialPostsFromVideoResponse from a dict
free_tool_generate_social_posts_from_video_response_from_dict = FreeToolGenerateSocialPostsFromVideoResponse.from_dict(free_tool_generate_social_posts_from_video_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


