# WorkspaceInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**hex_color** | **str** |  | 
**owner_id** | **int** |  | [optional] 
**access_status** | **str** |  | 

## Example

```python
from postboost.models.workspace_input import WorkspaceInput

# TODO update the JSON string below
json = "{}"
# create an instance of WorkspaceInput from a JSON string
workspace_input_instance = WorkspaceInput.from_json(json)
# print the JSON string representation of the object
print(WorkspaceInput.to_json())

# convert the object into a dict
workspace_input_dict = workspace_input_instance.to_dict()
# create an instance of WorkspaceInput from a dict
workspace_input_from_dict = WorkspaceInput.from_dict(workspace_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


