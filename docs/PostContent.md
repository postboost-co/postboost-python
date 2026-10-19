# PostContent

One item of a version's `content` array. The first item is always the post itself. What a second item means depends on the network:  - **Facebook Page, Instagram, LinkedIn** (profile and page): the second item's `body` is   published as the **first comment** under the post, right after the post goes live.   Only one comment is supported; further items are ignored. Facebook Stories take no comment. - **X, Threads, Bluesky, Mastodon, Pixelfed**: every additional item is published as the   next post of a **thread**, in order. - **All other networks** (YouTube, TikTok, Pinterest, Google Business Profile): only the   first item is published; additional items are ignored. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **str** | Post text/caption. For a second item on Facebook Page, Instagram or LinkedIn this is the first comment. | [optional] 
**url** | **str** | Link shown as a preview card on LinkedIn, Bluesky and Facebook Pages (Facebook builds the card from the page&#39;s own Open Graph tags). If omitted and the item has no media, the first link in &#x60;body&#x60; is used. | [optional] 
**media** | **List[int]** | Array of media IDs from the media library. | [optional] 
**video_thumbs** | **List[object]** |  | [optional] 

## Example

```python
from postboost.models.post_content import PostContent

# TODO update the JSON string below
json = "{}"
# create an instance of PostContent from a JSON string
post_content_instance = PostContent.from_json(json)
# print the JSON string representation of the object
print(PostContent.to_json())

# convert the object into a dict
post_content_dict = post_content_instance.to_dict()
# create an instance of PostContent from a dict
post_content_from_dict = PostContent.from_dict(post_content_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


