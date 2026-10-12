# PostOptionsTikTok

TikTok options. Every field is a map of `account-<account id>` to a value, so one post can carry different settings for several TikTok accounts. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**privacy_level** | **Dict[str, Optional[str]]** |  | [optional] 
**is_aigc** | **Dict[str, bool]** | TikTok&#39;s \&quot;AI-generated content\&quot; label. | [optional] 
**allow_comments** | **Dict[str, bool]** |  | [optional] 
**allow_duet** | **Dict[str, bool]** |  | [optional] 
**allow_stitch** | **Dict[str, bool]** |  | [optional] 
**auto_add_music** | **Dict[str, bool]** |  | [optional] 
**content_disclosure** | **Dict[str, bool]** | Discloses branded or promotional content; then set &#x60;brand_organic_toggle&#x60; and/or &#x60;brand_content_toggle&#x60;. | [optional] 
**brand_organic_toggle** | **Dict[str, bool]** |  | [optional] 
**brand_content_toggle** | **Dict[str, bool]** |  | [optional] 

## Example

```python
from postboost.models.post_options_tik_tok import PostOptionsTikTok

# TODO update the JSON string below
json = "{}"
# create an instance of PostOptionsTikTok from a JSON string
post_options_tik_tok_instance = PostOptionsTikTok.from_json(json)
# print the JSON string representation of the object
print(PostOptionsTikTok.to_json())

# convert the object into a dict
post_options_tik_tok_dict = post_options_tik_tok_instance.to_dict()
# create an instance of PostOptionsTikTok from a dict
post_options_tik_tok_from_dict = PostOptionsTikTok.from_dict(post_options_tik_tok_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


