# BlogToSocialCaption


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **int** | ID of the social account this caption was generated for. | [optional] 
**provider** | **str** | Social media platform identifier. | [optional] 
**content** | **str** | The generated caption text. &#x60;null&#x60; if generation failed for this account. | [optional] 
**character_count** | **int** | Character count of the generated content. &#x60;null&#x60; if generation failed. | [optional] 
**character_limit** | **int** | Maximum allowed character count for this platform. | [optional] 
**error** | **str** | Error message if caption generation failed for this account. &#x60;null&#x60; on success. | [optional] 

## Example

```python
from postboost.models.blog_to_social_caption import BlogToSocialCaption

# TODO update the JSON string below
json = "{}"
# create an instance of BlogToSocialCaption from a JSON string
blog_to_social_caption_instance = BlogToSocialCaption.from_json(json)
# print the JSON string representation of the object
print(BlogToSocialCaption.to_json())

# convert the object into a dict
blog_to_social_caption_dict = blog_to_social_caption_instance.to_dict()
# create an instance of BlogToSocialCaption from a dict
blog_to_social_caption_from_dict = BlogToSocialCaption.from_dict(blog_to_social_caption_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


