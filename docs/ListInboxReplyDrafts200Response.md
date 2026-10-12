# ListInboxReplyDrafts200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**links** | [**PaginationMetaLinks**](PaginationMetaLinks.md) |  | [optional] 
**meta** | [**PaginationMetaMeta**](PaginationMetaMeta.md) |  | [optional] 
**data** | [**List[InboxReplyDraft]**](InboxReplyDraft.md) |  | [optional] 

## Example

```python
from postboost.models.list_inbox_reply_drafts200_response import ListInboxReplyDrafts200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListInboxReplyDrafts200Response from a JSON string
list_inbox_reply_drafts200_response_instance = ListInboxReplyDrafts200Response.from_json(json)
# print the JSON string representation of the object
print(ListInboxReplyDrafts200Response.to_json())

# convert the object into a dict
list_inbox_reply_drafts200_response_dict = list_inbox_reply_drafts200_response_instance.to_dict()
# create an instance of ListInboxReplyDrafts200Response from a dict
list_inbox_reply_drafts200_response_from_dict = ListInboxReplyDrafts200Response.from_dict(list_inbox_reply_drafts200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


