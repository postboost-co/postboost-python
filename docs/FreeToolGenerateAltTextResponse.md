# FreeToolGenerateAltTextResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**alt_text** | **str** | The alt text, within the chosen length. | [optional] 
**short_alt_text** | **str** | A shorter alternative. | [optional] 
**credits_spent** | **int** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] 
**cached** | **bool** | True when the same request was answered before (free). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_alt_text_response import FreeToolGenerateAltTextResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateAltTextResponse from a JSON string
free_tool_generate_alt_text_response_instance = FreeToolGenerateAltTextResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateAltTextResponse.to_json())

# convert the object into a dict
free_tool_generate_alt_text_response_dict = free_tool_generate_alt_text_response_instance.to_dict()
# create an instance of FreeToolGenerateAltTextResponse from a dict
free_tool_generate_alt_text_response_from_dict = FreeToolGenerateAltTextResponse.from_dict(free_tool_generate_alt_text_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


