# FreeToolBuildAgentSkillRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**format** | **str** | skill_md (an Agent Skills SKILL.md), agents_md (AGENTS.md) or system_prompt. | [optional] [default to 'skill_md']
**name** | **str** | The skill name, normalised to lowercase letters, digits and hyphens and cut to 64 characters. | [optional] [default to 'postboost-social-media']
**brand** | **str** | The brand the agent works for; omitted when empty. | [optional] [default to '']
**tasks** | **List[str]** | What the agent does; the output keeps this enum&#39;s order. | [optional] [default to [draft_posts, schedule_posts]]
**networks** | **List[str]** | Networks to add character-limit rules for; none leaves the section out. | [optional] [default to []]
**autonomy** | **str** | How much the agent may do without asking. | [optional] [default to 'drafts_only']
**daily_cap** | **int** | Posts per day the agent may create; 0 adds no cap line. | [optional] [default to 5]
**brand_voice** | **bool** | Read the workspace brand voice before writing captions. | [optional] [default to True]
**connection** | **str** | connector (the OAuth MCP connector) or api_token (the advanced MCP server with an API key). | [optional] [default to 'connector']
**rules** | **List[str]** | Your own do&#39;s and don&#39;ts, one per item. | [optional] [default to []]

## Example

```python
from postboost.models.free_tool_build_agent_skill_request import FreeToolBuildAgentSkillRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolBuildAgentSkillRequest from a JSON string
free_tool_build_agent_skill_request_instance = FreeToolBuildAgentSkillRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolBuildAgentSkillRequest.to_json())

# convert the object into a dict
free_tool_build_agent_skill_request_dict = free_tool_build_agent_skill_request_instance.to_dict()
# create an instance of FreeToolBuildAgentSkillRequest from a dict
free_tool_build_agent_skill_request_from_dict = FreeToolBuildAgentSkillRequest.from_dict(free_tool_build_agent_skill_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


