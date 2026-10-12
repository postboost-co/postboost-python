# InboxMessage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Message UUID. | 
**direction** | **str** |  | 
**body** | **str** |  | 
**author** | [**InboxMessageAuthor**](InboxMessageAuthor.md) |  | [optional] 
**sentiment** | **str** |  | [optional] 
**ai_label** | **str** |  | [optional] 
**is_spam** | **bool** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.inbox_message import InboxMessage

# TODO update the JSON string below
json = "{}"
# create an instance of InboxMessage from a JSON string
inbox_message_instance = InboxMessage.from_json(json)
# print the JSON string representation of the object
print(InboxMessage.to_json())

# convert the object into a dict
inbox_message_dict = inbox_message_instance.to_dict()
# create an instance of InboxMessage from a dict
inbox_message_from_dict = InboxMessage.from_dict(inbox_message_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


