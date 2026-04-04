# BlogToSocialInput

At least one of `url` or (`title` + `excerpt`) must be provided. If both are given, direct values take priority over the scraped URL content. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | Blog post URL to scrape. Required if &#x60;title&#x60; and &#x60;excerpt&#x60; are not provided. | [optional] 
**title** | **str** | Blog post title. Required if &#x60;url&#x60; is not provided. | [optional] 
**excerpt** | **str** | Blog post summary or excerpt. Required if &#x60;url&#x60; is not provided. | [optional] 
**image_url** | **str** | Featured image URL for the blog post. When &#x60;create_post&#x60; is &#x60;true&#x60;, the image is imported into the workspace media library and attached to the draft post. If omitted in URL mode, the scraper attempts to extract the &#x60;og:image&#x60; meta tag.  | [optional] 
**platforms** | **List[str]** | Target social media platforms. Only connected accounts matching these platforms are used. If omitted, all connected accounts in the workspace are targeted.  | [optional] 
**account_ids** | **List[int]** | Specific account IDs to generate captions for. Takes precedence over &#x60;platforms&#x60; when both are provided.  | [optional] 
**tone** | **str** | Writing tone for all generated captions. | [optional] [default to 'engaging']
**content_length** | **str** | Desired length of the generated captions. | [optional] [default to 'medium']
**hashtags** | **str** | Hashtag quantity: none (0), few (1-3), some (3-5), many (5+). | [optional] [default to 'few']
**cta** | **str** | Call-to-action type appended to each caption. | [optional] [default to 'none']
**language** | **str** | Output language as an ISO 639-1 code (e.g. &#x60;en&#x60;, &#x60;de&#x60;, &#x60;fr&#x60;). Use &#x60;auto&#x60; to match the blog post&#39;s language automatically.  | [optional] [default to 'auto']
**custom_instructions** | **str** | Additional instructions appended to the AI prompt (e.g. \&quot;always mention our free tier\&quot;). | [optional] 
**create_post** | **bool** | When &#x60;true&#x60;, creates a draft post in the workspace with per-account caption versions. If an image is available, it is imported and attached to the post.  | [optional] [default to False]

## Example

```python
from postboost.models.blog_to_social_input import BlogToSocialInput

# TODO update the JSON string below
json = "{}"
# create an instance of BlogToSocialInput from a JSON string
blog_to_social_input_instance = BlogToSocialInput.from_json(json)
# print the JSON string representation of the object
print(BlogToSocialInput.to_json())

# convert the object into a dict
blog_to_social_input_dict = blog_to_social_input_instance.to_dict()
# create an instance of BlogToSocialInput from a dict
blog_to_social_input_from_dict = BlogToSocialInput.from_dict(blog_to_social_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


