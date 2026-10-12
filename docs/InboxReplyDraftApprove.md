# InboxReplyDraftApprove


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **str** | Edited text to send instead of the draft&#39;s. | [optional] 

## Example

```python
from postboost.models.inbox_reply_draft_approve import InboxReplyDraftApprove

# TODO update the JSON string below
json = "{}"
# create an instance of InboxReplyDraftApprove from a JSON string
inbox_reply_draft_approve_instance = InboxReplyDraftApprove.from_json(json)
# print the JSON string representation of the object
print(InboxReplyDraftApprove.to_json())

# convert the object into a dict
inbox_reply_draft_approve_dict = inbox_reply_draft_approve_instance.to_dict()
# create an instance of InboxReplyDraftApprove from a dict
inbox_reply_draft_approve_from_dict = InboxReplyDraftApprove.from_dict(inbox_reply_draft_approve_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


