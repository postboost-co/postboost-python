# BlogToSocialResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**blog_title** | **str** | The blog post title (scraped or provided directly). | [optional] 
**blog_excerpt** | **str** | A short excerpt from the blog post content. | [optional] 
**captions** | [**List[BlogToSocialCaption]**](BlogToSocialCaption.md) | Generated captions, one per target account. | [optional] 
**post_uuid** | **str** | UUID of the created draft post. Only present when &#x60;create_post&#x60; was &#x60;true&#x60;. | [optional] 
**media** | [**BlogToSocialMedia**](BlogToSocialMedia.md) |  | [optional] 
**credits_used** | **int** | Number of AI credits consumed by this request (one per successful caption). | [optional] 
**credits_remaining** | **int** | Remaining AI credits for the current billing period. &#x60;null&#x60; for unlimited plans. | [optional] 

## Example

```python
from postboost.models.blog_to_social_response import BlogToSocialResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BlogToSocialResponse from a JSON string
blog_to_social_response_instance = BlogToSocialResponse.from_json(json)
# print the JSON string representation of the object
print(BlogToSocialResponse.to_json())

# convert the object into a dict
blog_to_social_response_dict = blog_to_social_response_instance.to_dict()
# create an instance of BlogToSocialResponse from a dict
blog_to_social_response_from_dict = BlogToSocialResponse.from_dict(blog_to_social_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


