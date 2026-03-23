# DeleteWorkspacesBulkRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**workspaces** | **List[str]** |  | 

## Example

```python
from postboost.models.delete_workspaces_bulk_request import DeleteWorkspacesBulkRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteWorkspacesBulkRequest from a JSON string
delete_workspaces_bulk_request_instance = DeleteWorkspacesBulkRequest.from_json(json)
# print the JSON string representation of the object
print(DeleteWorkspacesBulkRequest.to_json())

# convert the object into a dict
delete_workspaces_bulk_request_dict = delete_workspaces_bulk_request_instance.to_dict()
# create an instance of DeleteWorkspacesBulkRequest from a dict
delete_workspaces_bulk_request_from_dict = DeleteWorkspacesBulkRequest.from_dict(delete_workspaces_bulk_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


