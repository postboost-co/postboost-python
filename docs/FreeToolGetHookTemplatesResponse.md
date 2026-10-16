# FreeToolGetHookTemplatesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hooks** | [**List[FreeToolGetHookTemplatesResponseHooksInner]**](FreeToolGetHookTemplatesResponseHooksInner.md) |  | [optional] 
**total** | **int** | Number of hooks returned. | [optional] 

## Example

```python
from postboost.models.free_tool_get_hook_templates_response import FreeToolGetHookTemplatesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetHookTemplatesResponse from a JSON string
free_tool_get_hook_templates_response_instance = FreeToolGetHookTemplatesResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetHookTemplatesResponse.to_json())

# convert the object into a dict
free_tool_get_hook_templates_response_dict = free_tool_get_hook_templates_response_instance.to_dict()
# create an instance of FreeToolGetHookTemplatesResponse from a dict
free_tool_get_hook_templates_response_from_dict = FreeToolGetHookTemplatesResponse.from_dict(free_tool_get_hook_templates_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


