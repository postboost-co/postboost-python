# InboxMessageAuthor


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**handle** | **str** |  | [optional] 
**avatar_url** | **str** |  | [optional] 

## Example

```python
from postboost.models.inbox_message_author import InboxMessageAuthor

# TODO update the JSON string below
json = "{}"
# create an instance of InboxMessageAuthor from a JSON string
inbox_message_author_instance = InboxMessageAuthor.from_json(json)
# print the JSON string representation of the object
print(InboxMessageAuthor.to_json())

# convert the object into a dict
inbox_message_author_dict = inbox_message_author_instance.to_dict()
# create an instance of InboxMessageAuthor from a dict
inbox_message_author_from_dict = InboxMessageAuthor.from_dict(inbox_message_author_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


