# FreeToolGenerateUsernamesResponseRules

The network's rules every name follows.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**min_length** | **int** |  | [optional] 
**max_length** | **int** |  | [optional] 
**separators** | **List[str]** |  | [optional] 

## Example

```python
from postboost.models.free_tool_generate_usernames_response_rules import FreeToolGenerateUsernamesResponseRules

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateUsernamesResponseRules from a JSON string
free_tool_generate_usernames_response_rules_instance = FreeToolGenerateUsernamesResponseRules.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateUsernamesResponseRules.to_json())

# convert the object into a dict
free_tool_generate_usernames_response_rules_dict = free_tool_generate_usernames_response_rules_instance.to_dict()
# create an instance of FreeToolGenerateUsernamesResponseRules from a dict
free_tool_generate_usernames_response_rules_from_dict = FreeToolGenerateUsernamesResponseRules.from_dict(free_tool_generate_usernames_response_rules_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


