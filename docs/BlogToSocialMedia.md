# BlogToSocialMedia

The imported featured image. Only present when `create_post` was `true` and an image was available.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Media library ID of the imported image. | [optional] 
**url** | **str** | Public URL of the imported image in the workspace media library. | [optional] 

## Example

```python
from postboost.models.blog_to_social_media import BlogToSocialMedia

# TODO update the JSON string below
json = "{}"
# create an instance of BlogToSocialMedia from a JSON string
blog_to_social_media_instance = BlogToSocialMedia.from_json(json)
# print the JSON string representation of the object
print(BlogToSocialMedia.to_json())

# convert the object into a dict
blog_to_social_media_dict = blog_to_social_media_instance.to_dict()
# create an instance of BlogToSocialMedia from a dict
blog_to_social_media_from_dict = BlogToSocialMedia.from_dict(blog_to_social_media_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


