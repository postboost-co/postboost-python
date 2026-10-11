# Mention


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**reference** | **int** | Write &#x60;{{mention:&lt;reference&gt;}}&#x60; in a post body to mention this entry; it is resolved to each network&#39;s identity at publish time. | 
**name** | **str** |  | 
**avatar** | **str** |  | [optional] 
**identities** | [**List[MentionIdentity]**](MentionIdentity.md) |  | [optional] 
**created_at** | **datetime** |  | 

## Example

```python
from postboost.models.mention import Mention

# TODO update the JSON string below
json = "{}"
# create an instance of Mention from a JSON string
mention_instance = Mention.from_json(json)
# print the JSON string representation of the object
print(Mention.to_json())

# convert the object into a dict
mention_dict = mention_instance.to_dict()
# create an instance of Mention from a dict
mention_from_dict = Mention.from_dict(mention_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


