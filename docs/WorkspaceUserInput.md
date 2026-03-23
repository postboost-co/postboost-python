# WorkspaceUserInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **int** |  | 
**role** | **str** |  | 
**can_approve** | **bool** |  | 
**is_owner** | **bool** |  | 

## Example

```python
from postboost.models.workspace_user_input import WorkspaceUserInput

# TODO update the JSON string below
json = "{}"
# create an instance of WorkspaceUserInput from a JSON string
workspace_user_input_instance = WorkspaceUserInput.from_json(json)
# print the JSON string representation of the object
print(WorkspaceUserInput.to_json())

# convert the object into a dict
workspace_user_input_dict = workspace_user_input_instance.to_dict()
# create an instance of WorkspaceUserInput from a dict
workspace_user_input_from_dict = WorkspaceUserInput.from_dict(workspace_user_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


