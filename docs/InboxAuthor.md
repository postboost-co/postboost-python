# InboxAuthor


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**handle** | **str** |  | [optional] 
**avatar_url** | **str** |  | [optional] 

## Example

```python
from postboost.models.inbox_author import InboxAuthor

# TODO update the JSON string below
json = "{}"
# create an instance of InboxAuthor from a JSON string
inbox_author_instance = InboxAuthor.from_json(json)
# print the JSON string representation of the object
print(InboxAuthor.to_json())

# convert the object into a dict
inbox_author_dict = inbox_author_instance.to_dict()
# create an instance of InboxAuthor from a dict
inbox_author_from_dict = InboxAuthor.from_dict(inbox_author_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


