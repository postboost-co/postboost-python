# Post


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**uuid** | **str** |  | [optional] 
**status** | [**PostStatus**](PostStatus.md) |  | [optional] 
**accounts** | [**List[Account]**](Account.md) |  | [optional] 
**versions** | [**List[PostVersion]**](PostVersion.md) |  | [optional] 
**tags** | [**List[Tag]**](Tag.md) |  | [optional] 
**scheduled_at** | **datetime** |  | [optional] 
**published_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**trashed** | **bool** |  | [optional] 

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


