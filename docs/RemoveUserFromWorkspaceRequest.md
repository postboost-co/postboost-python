# RemoveUserFromWorkspaceRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **int** |  | 

## Example

```python
from postboost.models.remove_user_from_workspace_request import RemoveUserFromWorkspaceRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RemoveUserFromWorkspaceRequest from a JSON string
remove_user_from_workspace_request_instance = RemoveUserFromWorkspaceRequest.from_json(json)
# print the JSON string representation of the object
print(RemoveUserFromWorkspaceRequest.to_json())

# convert the object into a dict
remove_user_from_workspace_request_dict = remove_user_from_workspace_request_instance.to_dict()
# create an instance of RemoveUserFromWorkspaceRequest from a dict
remove_user_from_workspace_request_from_dict = RemoveUserFromWorkspaceRequest.from_dict(remove_user_from_workspace_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


