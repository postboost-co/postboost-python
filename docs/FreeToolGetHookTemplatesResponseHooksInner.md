# FreeToolGetHookTemplatesResponseHooksInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | The hook, with &#x60;{topic}&#x60; filled in when a topic was given. | [optional] 
**template** | **str** | The template with its &#x60;{topic}&#x60; placeholder. | [optional] 
**category** | **str** | Hook style. | [optional] 
**networks** | **List[str]** | Networks the hook suits. | [optional] 

## Example

```python
from postboost.models.free_tool_get_hook_templates_response_hooks_inner import FreeToolGetHookTemplatesResponseHooksInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetHookTemplatesResponseHooksInner from a JSON string
free_tool_get_hook_templates_response_hooks_inner_instance = FreeToolGetHookTemplatesResponseHooksInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetHookTemplatesResponseHooksInner.to_json())

# convert the object into a dict
free_tool_get_hook_templates_response_hooks_inner_dict = free_tool_get_hook_templates_response_hooks_inner_instance.to_dict()
# create an instance of FreeToolGetHookTemplatesResponseHooksInner from a dict
free_tool_get_hook_templates_response_hooks_inner_from_dict = FreeToolGetHookTemplatesResponseHooksInner.from_dict(free_tool_get_hook_templates_response_hooks_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


