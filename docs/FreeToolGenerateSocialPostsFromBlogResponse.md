# FreeToolGenerateSocialPostsFromBlogResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**posts** | [**List[FreeToolGenerateSocialPostsFromBlogResponsePostsInner]**](FreeToolGenerateSocialPostsFromBlogResponsePostsInner.md) | One post per platform that came back, in the order asked. | [optional] 
**source** | [**FreeToolGenerateSocialPostsFromBlogResponseSource**](FreeToolGenerateSocialPostsFromBlogResponseSource.md) |  | [optional] 
**warnings** | [**List[FreeToolGenerateSocialPostsFromBlogResponseWarningsInner]**](FreeToolGenerateSocialPostsFromBlogResponseWarningsInner.md) |  | [optional] 
**credits_spent** | **int** | AI credits this call took from the workspace: one per post. | [optional] 

## Example

```python
from postboost.models.free_tool_generate_social_posts_from_blog_response import FreeToolGenerateSocialPostsFromBlogResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateSocialPostsFromBlogResponse from a JSON string
free_tool_generate_social_posts_from_blog_response_instance = FreeToolGenerateSocialPostsFromBlogResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateSocialPostsFromBlogResponse.to_json())

# convert the object into a dict
free_tool_generate_social_posts_from_blog_response_dict = free_tool_generate_social_posts_from_blog_response_instance.to_dict()
# create an instance of FreeToolGenerateSocialPostsFromBlogResponse from a dict
free_tool_generate_social_posts_from_blog_response_from_dict = FreeToolGenerateSocialPostsFromBlogResponse.from_dict(free_tool_generate_social_posts_from_blog_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


