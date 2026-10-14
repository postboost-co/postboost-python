# FreeToolCountCharactersResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hashtags** | **int** | Hashtags in the text (Instagram allows 5 per post in PostBoost). | [optional] 
**networks** | [**List[FreeToolCountCharactersResponseNetworksInner]**](FreeToolCountCharactersResponseNetworksInner.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_count_characters_response import FreeToolCountCharactersResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCountCharactersResponse from a JSON string
free_tool_count_characters_response_instance = FreeToolCountCharactersResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCountCharactersResponse.to_json())

# convert the object into a dict
free_tool_count_characters_response_dict = free_tool_count_characters_response_instance.to_dict()
# create an instance of FreeToolCountCharactersResponse from a dict
free_tool_count_characters_response_from_dict = FreeToolCountCharactersResponse.from_dict(free_tool_count_characters_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


