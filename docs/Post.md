# Post


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**uuid** | **str** |  | 
**status** | [**PostStatus**](PostStatus.md) |  | 
**publish_progress** | [**PublishProgress**](PublishProgress.md) | Only present while the post is publishing. | [optional] 
**accounts** | [**List[Account]**](Account.md) |  | 
**versions** | [**List[PostVersion]**](PostVersion.md) |  | 
**tags** | [**List[Tag]**](Tag.md) |  | 
**scheduled_at** | **str** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). | [optional] 
**published_at** | **str** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). | [optional] 
**created_at** | **str** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). | 
**trashed** | **bool** |  | 

## Example

```python
from postboost.models.post import Post

# TODO update the JSON string below
json = "{}"
# create an instance of Post from a JSON string
post_instance = Post.from_json(json)
# print the JSON string representation of the object
print(Post.to_json())

# convert the object into a dict
post_dict = post_instance.to_dict()
# create an instance of Post from a dict
post_from_dict = Post.from_dict(post_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


