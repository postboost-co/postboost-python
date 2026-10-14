# FreeToolGenerateFancyTextRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**style** | **str** | One style only; every style when omitted. | [optional] 

## Example

```python
from postboost.models.free_tool_generate_fancy_text_request import FreeToolGenerateFancyTextRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateFancyTextRequest from a JSON string
free_tool_generate_fancy_text_request_instance = FreeToolGenerateFancyTextRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateFancyTextRequest.to_json())

# convert the object into a dict
free_tool_generate_fancy_text_request_dict = free_tool_generate_fancy_text_request_instance.to_dict()
# create an instance of FreeToolGenerateFancyTextRequest from a dict
free_tool_generate_fancy_text_request_from_dict = FreeToolGenerateFancyTextRequest.from_dict(free_tool_generate_fancy_text_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


