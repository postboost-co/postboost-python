# GetInboxConversation200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**InboxConversation**](InboxConversation.md) |  | 

## Example

```python
from postboost.models.get_inbox_conversation200_response import GetInboxConversation200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetInboxConversation200Response from a JSON string
get_inbox_conversation200_response_instance = GetInboxConversation200Response.from_json(json)
# print the JSON string representation of the object
print(GetInboxConversation200Response.to_json())

# convert the object into a dict
get_inbox_conversation200_response_dict = get_inbox_conversation200_response_instance.to_dict()
# create an instance of GetInboxConversation200Response from a dict
get_inbox_conversation200_response_from_dict = GetInboxConversation200Response.from_dict(get_inbox_conversation200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


