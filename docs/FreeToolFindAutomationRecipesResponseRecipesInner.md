# FreeToolFindAutomationRecipesResponseRecipesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slug** | **str** | Stable key of the recipe, also its anchor on the page. | [optional] 
**title** | **str** | What the recipe does. | [optional] 
**trigger** | **str** | What starts it. | [optional] 
**goal** | **str** | The result in one or two sentences. | [optional] 
**native** | [**FreeToolFindAutomationRecipesResponseRecipesInnerNative**](FreeToolFindAutomationRecipesResponseRecipesInnerNative.md) |  | [optional] 
**api_operations** | [**List[FreeToolFindAutomationRecipesResponseRecipesInnerApiOperationsInner]**](FreeToolFindAutomationRecipesResponseRecipesInnerApiOperationsInner.md) | The PostBoost API operations the recipe calls. | [optional] 
**steps** | [**FreeToolFindAutomationRecipesResponseRecipesInnerSteps**](FreeToolFindAutomationRecipesResponseRecipesInnerSteps.md) |  | [optional] 
**n8n_workflow** | **Dict[str, object]** | Importable n8n workflow (core nodes only; add a Header Auth credential named \&quot;PostBoost API token\&quot;) when &#x60;platform&#x60; is &#x60;n8n&#x60;; null otherwise. | [optional] 

## Example

```python
from postboost.models.free_tool_find_automation_recipes_response_recipes_inner import FreeToolFindAutomationRecipesResponseRecipesInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolFindAutomationRecipesResponseRecipesInner from a JSON string
free_tool_find_automation_recipes_response_recipes_inner_instance = FreeToolFindAutomationRecipesResponseRecipesInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolFindAutomationRecipesResponseRecipesInner.to_json())

# convert the object into a dict
free_tool_find_automation_recipes_response_recipes_inner_dict = free_tool_find_automation_recipes_response_recipes_inner_instance.to_dict()
# create an instance of FreeToolFindAutomationRecipesResponseRecipesInner from a dict
free_tool_find_automation_recipes_response_recipes_inner_from_dict = FreeToolFindAutomationRecipesResponseRecipesInner.from_dict(free_tool_find_automation_recipes_response_recipes_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


