# PostVersion


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **int** | Use &#x60;0&#x60; for the original/default version. | 
**is_original** | **bool** | Must be &#x60;true&#x60; for the first version. | 
**synced_with** | **int** | Account ID of the version this version follows (&#x60;0&#x60; &#x3D; the original), or null when it is edited independently. Ignored on the original version. | [optional] 
**content** | [**List[PostContent]**](PostContent.md) | Ordered content items. Item 0 is the post. Item 1 is the first comment on Facebook Page, Instagram and LinkedIn, or the next thread post on X, Threads, Bluesky, Mastodon and Pixelfed. See &#x60;PostContent&#x60;.  | 
**options** | [**PostVersionOptions**](PostVersionOptions.md) |  | [optional] 

## Example

```python
from postboost.models.post_version import PostVersion

# TODO update the JSON string below
json = "{}"
# create an instance of PostVersion from a JSON string
post_version_instance = PostVersion.from_json(json)
# print the JSON string representation of the object
print(PostVersion.to_json())

# convert the object into a dict
post_version_dict = post_version_instance.to_dict()
# create an instance of PostVersion from a dict
post_version_from_dict = PostVersion.from_dict(post_version_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


