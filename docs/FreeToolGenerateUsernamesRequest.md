# FreeToolGenerateUsernamesRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Your name, brand or a few keywords. Accents are dropped; only Latin letters and digits are used. | 
**network** | **str** | Whose username rules apply (Threads uses your Instagram username). | [optional] [default to 'instagram']
**style** | **str** | Which word list to mix in. | [optional] [default to 'clean']
**numbers** | **bool** | Allow a number at the end of some names. | [optional] [default to False]
**seed** | **int** | The same input and seed give the same list; change it for more ideas. | [optional] [default to 0]

## Example

```python
from postboost.models.free_tool_generate_usernames_request import FreeToolGenerateUsernamesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateUsernamesRequest from a JSON string
free_tool_generate_usernames_request_instance = FreeToolGenerateUsernamesRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateUsernamesRequest.to_json())

# convert the object into a dict
free_tool_generate_usernames_request_dict = free_tool_generate_usernames_request_instance.to_dict()
# create an instance of FreeToolGenerateUsernamesRequest from a dict
free_tool_generate_usernames_request_from_dict = FreeToolGenerateUsernamesRequest.from_dict(free_tool_generate_usernames_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


