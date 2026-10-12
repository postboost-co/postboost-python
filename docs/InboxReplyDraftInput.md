# InboxReplyDraftInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **str** | The reply text. Limit depends on the network. | 
**in_reply_to** | **str** | Message &#x60;id&#x60; to reply to; defaults to the latest incoming message. | [optional] 

## Example

```python
from postboost.models.inbox_reply_draft_input import InboxReplyDraftInput

# TODO update the JSON string below
json = "{}"
# create an instance of InboxReplyDraftInput from a JSON string
inbox_reply_draft_input_instance = InboxReplyDraftInput.from_json(json)
# print the JSON string representation of the object
print(InboxReplyDraftInput.to_json())

# convert the object into a dict
inbox_reply_draft_input_dict = inbox_reply_draft_input_instance.to_dict()
# create an instance of InboxReplyDraftInput from a dict
inbox_reply_draft_input_from_dict = InboxReplyDraftInput.from_dict(inbox_reply_draft_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


