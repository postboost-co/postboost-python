# FreeToolCountCharactersRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | The post text, up to 10,000 characters (twice the longest network limit); 5,000 without an API token. | [optional] [default to '']
**network** | **str** | Count for one network only; all networks when omitted. | [optional] 

## Example

```python
from postboost.models.free_tool_count_characters_request import FreeToolCountCharactersRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCountCharactersRequest from a JSON string
free_tool_count_characters_request_instance = FreeToolCountCharactersRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCountCharactersRequest.to_json())

# convert the object into a dict
free_tool_count_characters_request_dict = free_tool_count_characters_request_instance.to_dict()
# create an instance of FreeToolCountCharactersRequest from a dict
free_tool_count_characters_request_from_dict = FreeToolCountCharactersRequest.from_dict(free_tool_count_characters_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


