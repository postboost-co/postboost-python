# FreeToolFindAutomationRecipesResponseRecipesInnerSteps

Steps per platform, naming its generic HTTP module; only the requested platform when `platform` is set.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**n8n** | **List[str]** |  | [optional] 
**zapier** | **List[str]** |  | [optional] 
**make** | **List[str]** |  | [optional] 

## Example

```python
from postboost.models.free_tool_find_automation_recipes_response_recipes_inner_steps import FreeToolFindAutomationRecipesResponseRecipesInnerSteps

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolFindAutomationRecipesResponseRecipesInnerSteps from a JSON string
free_tool_find_automation_recipes_response_recipes_inner_steps_instance = FreeToolFindAutomationRecipesResponseRecipesInnerSteps.from_json(json)
# print the JSON string representation of the object
print(FreeToolFindAutomationRecipesResponseRecipesInnerSteps.to_json())

# convert the object into a dict
free_tool_find_automation_recipes_response_recipes_inner_steps_dict = free_tool_find_automation_recipes_response_recipes_inner_steps_instance.to_dict()
# create an instance of FreeToolFindAutomationRecipesResponseRecipesInnerSteps from a dict
free_tool_find_automation_recipes_response_recipes_inner_steps_from_dict = FreeToolFindAutomationRecipesResponseRecipesInnerSteps.from_dict(free_tool_find_automation_recipes_response_recipes_inner_steps_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


