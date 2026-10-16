# FreeToolGenerateHooksResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hooks** | [**List[FreeToolGenerateHooksResponseHooksInner]**](FreeToolGenerateHooksResponseHooksInner.md) | &#x60;count&#x60; hooks in several styles. | [optional] 
**notice** | **str** | Only while AI is switched off: the hooks are templates from the free library (getHookTemplates) with the topic filled in, free of charge. | [optional] 
**credits_spent** | **int** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] 
**cached** | **bool** | True when the same request was answered before (free). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_hooks_response import FreeToolGenerateHooksResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateHooksResponse from a JSON string
free_tool_generate_hooks_response_instance = FreeToolGenerateHooksResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateHooksResponse.to_json())

# convert the object into a dict
free_tool_generate_hooks_response_dict = free_tool_generate_hooks_response_instance.to_dict()
# create an instance of FreeToolGenerateHooksResponse from a dict
free_tool_generate_hooks_response_from_dict = FreeToolGenerateHooksResponse.from_dict(free_tool_generate_hooks_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


