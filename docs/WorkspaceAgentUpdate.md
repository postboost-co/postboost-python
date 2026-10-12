# WorkspaceAgentUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**enabled** | **bool** |  | [optional] 
**schedule** | **str** |  | [optional] 
**settings** | [**WorkspaceAgentSettings**](WorkspaceAgentSettings.md) |  | [optional] 

## Example

```python
from postboost.models.workspace_agent_update import WorkspaceAgentUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of WorkspaceAgentUpdate from a JSON string
workspace_agent_update_instance = WorkspaceAgentUpdate.from_json(json)
# print the JSON string representation of the object
print(WorkspaceAgentUpdate.to_json())

# convert the object into a dict
workspace_agent_update_dict = workspace_agent_update_instance.to_dict()
# create an instance of WorkspaceAgentUpdate from a dict
workspace_agent_update_from_dict = WorkspaceAgentUpdate.from_dict(workspace_agent_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


