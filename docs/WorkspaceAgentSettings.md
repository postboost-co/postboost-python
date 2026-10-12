# WorkspaceAgentSettings

Pre-publish checker settings.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**horizon_hours** | **int** | Check posts scheduled within this many hours. | [optional] [default to 24]
**check_links** | **bool** | Flag links in captions that answer an HTTP error. | [optional] [default to True]
**banned_phrases** | **List[str]** | Phrases to propose removing from captions. | [optional] [default to []]
**ai_review** | **bool** | Ask AI to review captions (one AI credit per reviewed post). | [optional] [default to False]
**max_ai_reviews_per_run** | **int** |  | [optional] [default to 10]

## Example

```python
from postboost.models.workspace_agent_settings import WorkspaceAgentSettings

# TODO update the JSON string below
json = "{}"
# create an instance of WorkspaceAgentSettings from a JSON string
workspace_agent_settings_instance = WorkspaceAgentSettings.from_json(json)
# print the JSON string representation of the object
print(WorkspaceAgentSettings.to_json())

# convert the object into a dict
workspace_agent_settings_dict = workspace_agent_settings_instance.to_dict()
# create an instance of WorkspaceAgentSettings from a dict
workspace_agent_settings_from_dict = WorkspaceAgentSettings.from_dict(workspace_agent_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


