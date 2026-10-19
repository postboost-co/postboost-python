# FreeToolGenerateUsernamesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**network** | **str** |  | [optional] 
**style** | **str** |  | [optional] 
**seed** | **int** |  | [optional] 
**usernames** | [**List[FreeToolGenerateUsernamesResponseUsernamesInner]**](FreeToolGenerateUsernamesResponseUsernamesInner.md) | Up to 30 names, each valid for the network. Not checked for availability: open the profile URL to see whether a name is taken. | [optional] 
**rules** | [**FreeToolGenerateUsernamesResponseRules**](FreeToolGenerateUsernamesResponseRules.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_generate_usernames_response import FreeToolGenerateUsernamesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateUsernamesResponse from a JSON string
free_tool_generate_usernames_response_instance = FreeToolGenerateUsernamesResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateUsernamesResponse.to_json())

# convert the object into a dict
free_tool_generate_usernames_response_dict = free_tool_generate_usernames_response_instance.to_dict()
# create an instance of FreeToolGenerateUsernamesResponse from a dict
free_tool_generate_usernames_response_from_dict = FreeToolGenerateUsernamesResponse.from_dict(free_tool_generate_usernames_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


