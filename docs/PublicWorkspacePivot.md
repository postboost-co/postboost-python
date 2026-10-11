# PublicWorkspacePivot

The caller's membership in the workspace.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | [optional] 
**can_approve** | **bool** |  | [optional] 
**joined_at** | **str** |  | [optional] 

## Example

```python
from postboost.models.public_workspace_pivot import PublicWorkspacePivot

# TODO update the JSON string below
json = "{}"
# create an instance of PublicWorkspacePivot from a JSON string
public_workspace_pivot_instance = PublicWorkspacePivot.from_json(json)
# print the JSON string representation of the object
print(PublicWorkspacePivot.to_json())

# convert the object into a dict
public_workspace_pivot_dict = public_workspace_pivot_instance.to_dict()
# create an instance of PublicWorkspacePivot from a dict
public_workspace_pivot_from_dict = PublicWorkspacePivot.from_dict(public_workspace_pivot_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


