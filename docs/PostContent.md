# PostContent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **str** | Post text/caption. | [optional] 
**url** | **str** |  | [optional] 
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


