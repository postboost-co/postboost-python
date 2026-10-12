# WorkspaceAgentInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**name** | **str** |  | [optional] 
**enabled** | **bool** |  | [optional] [default to True]
**schedule** | **str** |  | [optional] [default to 'hourly']
**settings** | [**WorkspaceAgentSettings**](WorkspaceAgentSettings.md) |  | [optional] 

## Example

```python
from postboost.models.workspace_agent_input import WorkspaceAgentInput

# TODO update the JSON string below
json = "{}"
# create an instance of WorkspaceAgentInput from a JSON string
workspace_agent_input_instance = WorkspaceAgentInput.from_json(json)
# print the JSON string representation of the object
print(WorkspaceAgentInput.to_json())

# convert the object into a dict
workspace_agent_input_dict = workspace_agent_input_instance.to_dict()
# create an instance of WorkspaceAgentInput from a dict
workspace_agent_input_from_dict = WorkspaceAgentInput.from_dict(workspace_agent_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


