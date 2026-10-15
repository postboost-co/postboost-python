# FreeToolCleanTextResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | [optional] 
**changes** | [**List[FreeToolCleanTextResponseChangesInner]**](FreeToolCleanTextResponseChangesInner.md) | One entry per change type that changed something. | [optional] 
**flags** | [**List[FreeToolCleanTextResponseFlagsInner]**](FreeToolCleanTextResponseFlagsInner.md) | AI phrases in the cleaned text, by offset (Unicode code points). | [optional] 

## Example

```python
from postboost.models.free_tool_clean_text_response import FreeToolCleanTextResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCleanTextResponse from a JSON string
free_tool_clean_text_response_instance = FreeToolCleanTextResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCleanTextResponse.to_json())

# convert the object into a dict
free_tool_clean_text_response_dict = free_tool_clean_text_response_instance.to_dict()
# create an instance of FreeToolCleanTextResponse from a dict
free_tool_clean_text_response_from_dict = FreeToolCleanTextResponse.from_dict(free_tool_clean_text_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


