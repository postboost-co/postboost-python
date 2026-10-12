# InboxReplyDraft


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Draft UUID. | 
**status** | **str** |  | 
**body** | **str** |  | 
**source** | **str** |  | 
**conversation_id** | **str** |  | [optional] 
**provider** | **str** |  | [optional] 
**in_reply_to** | **object** | The incoming message this replies to (same shape as &#x60;InboxMessage&#x60;). | [optional] 
**created_by** | **str** | Name of the user whose API key wrote the draft. | [optional] 
**reviewed_by** | **str** |  | [optional] 
**reviewed_at** | **datetime** |  | [optional] 
**sent_message_id** | **str** | The sent reply&#39;s message UUID, once sent. | [optional] 
**error** | **str** | Why sending failed. | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.inbox_reply_draft import InboxReplyDraft

# TODO update the JSON string below
json = "{}"
# create an instance of InboxReplyDraft from a JSON string
inbox_reply_draft_instance = InboxReplyDraft.from_json(json)
# print the JSON string representation of the object
print(InboxReplyDraft.to_json())

# convert the object into a dict
inbox_reply_draft_dict = inbox_reply_draft_instance.to_dict()
# create an instance of InboxReplyDraft from a dict
inbox_reply_draft_from_dict = InboxReplyDraft.from_dict(inbox_reply_draft_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


