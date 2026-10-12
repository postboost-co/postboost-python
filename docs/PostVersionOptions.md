# PostVersionOptions

Platform-specific publishing options, keyed by network (`tiktok`, `youtube`, `instagram`, `mastodon`, …). Options of networks the post does not publish to are ignored. To label a post as AI-generated on every network that supports it, send `ai_generated` on the post instead of setting `tiktok.is_aigc`, `youtube.contains_synthetic_media` or `instagram.ai_generated` yourself. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tiktok** | [**PostOptionsTikTok**](PostOptionsTikTok.md) |  | [optional] 
**youtube** | [**PostOptionsYoutube**](PostOptionsYoutube.md) |  | [optional] 
**instagram** | [**PostOptionsInstagram**](PostOptionsInstagram.md) |  | [optional] 
**instagram_standalone** | [**PostOptionsInstagram**](PostOptionsInstagram.md) |  | [optional] 

## Example

```python
from postboost.models.post_version_options import PostVersionOptions

# TODO update the JSON string below
json = "{}"
# create an instance of PostVersionOptions from a JSON string
post_version_options_instance = PostVersionOptions.from_json(json)
# print the JSON string representation of the object
print(PostVersionOptions.to_json())

# convert the object into a dict
post_version_options_dict = post_version_options_instance.to_dict()
# create an instance of PostVersionOptions from a dict
post_version_options_from_dict = PostVersionOptions.from_dict(post_version_options_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


