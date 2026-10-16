# FreeToolGenerateSocialPostsFromBlogResponsePostsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **str** |  | [optional] 
**text** | **str** | The post, cut at a sentence end when the model ran over the limit. | [optional] 
**hashtags** | **List[str]** | Hashtags in the text, with #. | [optional] 
**characters** | **int** | Length as the network counts it (X weighs links as 23, YouTube counts bytes). | [optional] 
**limit** | **int** | The network&#39;s text limit. | [optional] 

## Example

```python
from postboost.models.free_tool_generate_social_posts_from_blog_response_posts_inner import FreeToolGenerateSocialPostsFromBlogResponsePostsInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateSocialPostsFromBlogResponsePostsInner from a JSON string
free_tool_generate_social_posts_from_blog_response_posts_inner_instance = FreeToolGenerateSocialPostsFromBlogResponsePostsInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateSocialPostsFromBlogResponsePostsInner.to_json())

# convert the object into a dict
free_tool_generate_social_posts_from_blog_response_posts_inner_dict = free_tool_generate_social_posts_from_blog_response_posts_inner_instance.to_dict()
# create an instance of FreeToolGenerateSocialPostsFromBlogResponsePostsInner from a dict
free_tool_generate_social_posts_from_blog_response_posts_inner_from_dict = FreeToolGenerateSocialPostsFromBlogResponsePostsInner.from_dict(free_tool_generate_social_posts_from_blog_response_posts_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


