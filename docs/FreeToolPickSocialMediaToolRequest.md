# FreeToolPickSocialMediaToolRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**needs** | **List[str]** | What you need: team_dashboard (Scheduling dashboard for a team), rest_openapi (REST API with a published OpenAPI spec), sdks (At least one official SDK), mcp (MCP server for AI agents), webhooks (Webhooks), free_tier (Free hosted plan), zapier (Native Zapier app), n8n (Native n8n node), make (Native Make app). Required unless use_case is set. | [optional] 
**use_case** | **str** | A shortcut used when needs is left out: team_scheduling (team_dashboard, free_tier), build_app (rest_openapi, sdks, webhooks), ai_agent (mcp, rest_openapi). | [optional] 

## Example

```python
from postboost.models.free_tool_pick_social_media_tool_request import FreeToolPickSocialMediaToolRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPickSocialMediaToolRequest from a JSON string
free_tool_pick_social_media_tool_request_instance = FreeToolPickSocialMediaToolRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolPickSocialMediaToolRequest.to_json())

# convert the object into a dict
free_tool_pick_social_media_tool_request_dict = free_tool_pick_social_media_tool_request_instance.to_dict()
# create an instance of FreeToolPickSocialMediaToolRequest from a dict
free_tool_pick_social_media_tool_request_from_dict = FreeToolPickSocialMediaToolRequest.from_dict(free_tool_pick_social_media_tool_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


