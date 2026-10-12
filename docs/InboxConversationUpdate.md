# InboxConversationUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**unread** | **bool** |  | [optional] 

## Example

```python
from postboost.models.inbox_conversation_update import InboxConversationUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of InboxConversationUpdate from a JSON string
inbox_conversation_update_instance = InboxConversationUpdate.from_json(json)
# print the JSON string representation of the object
print(InboxConversationUpdate.to_json())

# convert the object into a dict
inbox_conversation_update_dict = inbox_conversation_update_instance.to_dict()
# create an instance of InboxConversationUpdate from a dict
inbox_conversation_update_from_dict = InboxConversationUpdate.from_dict(inbox_conversation_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


