# InboxConversation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Conversation UUID. | 
**provider** | **str** |  | 
**type** | **str** |  | [optional] 
**status** | **str** |  | 
**unread** | **bool** |  | 
**sentiment** | **str** |  | [optional] 
**ai_label** | **str** |  | [optional] 
**is_spam** | **bool** |  | [optional] 
**is_hidden** | **bool** |  | [optional] 
**provider_post_id** | **str** |  | [optional] 
**account** | [**InboxConversationAccount**](InboxConversationAccount.md) |  | [optional] 
**author** | [**InboxMessageAuthor**](InboxMessageAuthor.md) |  | [optional] 
**latest_message** | **object** | Only in lists. | [optional] 
**messages** | [**List[InboxMessage]**](InboxMessage.md) | Only on &#x60;GET inbox/conversations/{conversationId}&#x60;. | [optional] 
**last_message_at** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.inbox_conversation import InboxConversation

# TODO update the JSON string below
json = "{}"
# create an instance of InboxConversation from a JSON string
inbox_conversation_instance = InboxConversation.from_json(json)
# print the JSON string representation of the object
print(InboxConversation.to_json())

# convert the object into a dict
inbox_conversation_dict = inbox_conversation_instance.to_dict()
# create an instance of InboxConversation from a dict
inbox_conversation_from_dict = InboxConversation.from_dict(inbox_conversation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


