# FreeToolBuildAgentSkillResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**format** | **str** |  | [optional] 
**filename** | **str** |  | [optional] 
**content** | **str** | The file, in Markdown. | [optional] 
**install** | **List[str]** | Where to put the file. | [optional] 
**tools_used** | **List[str]** | The connector tool names the content names, in first-appearance order; empty with api_token. | [optional] 
**lines** | **int** |  | [optional] 
**warnings** | [**List[FreeToolCheckPostResponseNetworksInnerErrorsInner]**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: name_normalized, task_limited_by_autonomy, autonomy_high, too_long. | [optional] 

## Example

```python
from postboost.models.free_tool_build_agent_skill_response import FreeToolBuildAgentSkillResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolBuildAgentSkillResponse from a JSON string
free_tool_build_agent_skill_response_instance = FreeToolBuildAgentSkillResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolBuildAgentSkillResponse.to_json())

# convert the object into a dict
free_tool_build_agent_skill_response_dict = free_tool_build_agent_skill_response_instance.to_dict()
# create an instance of FreeToolBuildAgentSkillResponse from a dict
free_tool_build_agent_skill_response_from_dict = FreeToolBuildAgentSkillResponse.from_dict(free_tool_build_agent_skill_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


