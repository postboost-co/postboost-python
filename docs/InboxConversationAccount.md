# InboxConversationAccount


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**uuid** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**provider** | **str** |  | [optional] 

## Example

```python
from postboost.models.inbox_conversation_account import InboxConversationAccount

# TODO update the JSON string below
json = "{}"
# create an instance of InboxConversationAccount from a JSON string
inbox_conversation_account_instance = InboxConversationAccount.from_json(json)
# print the JSON string representation of the object
print(InboxConversationAccount.to_json())

# convert the object into a dict
inbox_conversation_account_dict = inbox_conversation_account_instance.to_dict()
# create an instance of InboxConversationAccount from a dict
inbox_conversation_account_from_dict = InboxConversationAccount.from_dict(inbox_conversation_account_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


