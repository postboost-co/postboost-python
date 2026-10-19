# FreeToolFindAutomationRecipesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** | Number of recipes returned. | [optional] 
**recipes** | [**List[FreeToolFindAutomationRecipesResponseRecipesInner]**](FreeToolFindAutomationRecipesResponseRecipesInner.md) |  | [optional] 
**last_verified** | **date** | When the recipes were last checked against the API and the platforms. | [optional] 

## Example

```python
from postboost.models.free_tool_find_automation_recipes_response import FreeToolFindAutomationRecipesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolFindAutomationRecipesResponse from a JSON string
free_tool_find_automation_recipes_response_instance = FreeToolFindAutomationRecipesResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolFindAutomationRecipesResponse.to_json())

# convert the object into a dict
free_tool_find_automation_recipes_response_dict = free_tool_find_automation_recipes_response_instance.to_dict()
# create an instance of FreeToolFindAutomationRecipesResponse from a dict
free_tool_find_automation_recipes_response_from_dict = FreeToolFindAutomationRecipesResponse.from_dict(free_tool_find_automation_recipes_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


