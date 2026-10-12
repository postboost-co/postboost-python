# PostOptionsYoutube

YouTube options. The video title is required.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | [optional] 
**status** | **str** |  | [optional] [default to 'public']
**made_for_kids** | **bool** |  | [optional] [default to False]
**contains_synthetic_media** | **bool** | YouTube&#39;s \&quot;altered or synthetic content\&quot; disclosure. Set by &#x60;ai_generated&#x60;. | [optional] [default to False]

## Example

```python
from postboost.models.post_options_youtube import PostOptionsYoutube

# TODO update the JSON string below
json = "{}"
# create an instance of PostOptionsYoutube from a JSON string
post_options_youtube_instance = PostOptionsYoutube.from_json(json)
# print the JSON string representation of the object
print(PostOptionsYoutube.to_json())

# convert the object into a dict
post_options_youtube_dict = post_options_youtube_instance.to_dict()
# create an instance of PostOptionsYoutube from a dict
post_options_youtube_from_dict = PostOptionsYoutube.from_dict(post_options_youtube_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


