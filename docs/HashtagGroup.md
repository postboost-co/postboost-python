# HashtagGroup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Hashtag group UUID. | 
**name** | **str** |  | 
**content** | **str** |  | 

## Example

```python
from postboost.models.hashtag_group import HashtagGroup

# TODO update the JSON string below
json = "{}"
# create an instance of HashtagGroup from a JSON string
hashtag_group_instance = HashtagGroup.from_json(json)
# print the JSON string representation of the object
print(HashtagGroup.to_json())

# convert the object into a dict
hashtag_group_dict = hashtag_group_instance.to_dict()
# create an instance of HashtagGroup from a dict
hashtag_group_from_dict = HashtagGroup.from_dict(hashtag_group_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


