# WorkspaceAgent


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | 
**type** | **str** |  | 
**name** | **str** |  | 
**enabled** | **bool** |  | 
**schedule** | **str** |  | 
**settings** | [**WorkspaceAgentSettings**](WorkspaceAgentSettings.md) |  | 
**last_run_at** | **datetime** |  | 
**next_run_at** | **datetime** |  | 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.workspace_agent import WorkspaceAgent

# TODO update the JSON string below
json = "{}"
# create an instance of WorkspaceAgent from a JSON string
workspace_agent_instance = WorkspaceAgent.from_json(json)
# print the JSON string representation of the object
print(WorkspaceAgent.to_json())

# convert the object into a dict
workspace_agent_dict = workspace_agent_instance.to_dict()
# create an instance of WorkspaceAgent from a dict
workspace_agent_from_dict = WorkspaceAgent.from_dict(workspace_agent_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


