# FreeToolGenerateSocialPostsFromBlogRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | Public http(s) address of the blog post. Give &#x60;url&#x60; or &#x60;text&#x60;. | [optional] 
**text** | **str** | The blog post itself, instead of &#x60;url&#x60;. | [optional] 
**platforms** | **List[str]** | Networks to write for, at most 4 per call (one AI credit each). | 
**tone** | **str** |  | [optional] [default to 'casual']
**length** | **str** |  | [optional] [default to 'short']
**hashtags** | **str** | How many hashtags to include. | [optional] [default to 'no']
**cta** | **str** | Call to action to end with. | [optional] [default to 'no']
**workspace** | **str** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_social_posts_from_blog_request import FreeToolGenerateSocialPostsFromBlogRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateSocialPostsFromBlogRequest from a JSON string
free_tool_generate_social_posts_from_blog_request_instance = FreeToolGenerateSocialPostsFromBlogRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateSocialPostsFromBlogRequest.to_json())

# convert the object into a dict
free_tool_generate_social_posts_from_blog_request_dict = free_tool_generate_social_posts_from_blog_request_instance.to_dict()
# create an instance of FreeToolGenerateSocialPostsFromBlogRequest from a dict
free_tool_generate_social_posts_from_blog_request_from_dict = FreeToolGenerateSocialPostsFromBlogRequest.from_dict(free_tool_generate_social_posts_from_blog_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


