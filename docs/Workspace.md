# Workspace


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | 
**name** | **str** |  | 
**hex_color** | **str** | Deprecated. Workspaces no longer have a colour (workspaces now use &#x60;avatar&#x60;); the API returns the constant &#x60;4f46e5&#x60; so existing clients keep working. Will be removed in API v2. | [optional] 
**avatar** | **str** | URL of the workspace avatar, or null when none is set. Supersedes &#x60;hex_color&#x60;. | [optional] 
**owner** | [**User**](User.md) |  | [optional] 
**access_status** | **str** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from postboost.models.workspace import Workspace

# TODO update the JSON string below
json = "{}"
# create an instance of Workspace from a JSON string
workspace_instance = Workspace.from_json(json)
# print the JSON string representation of the object
print(Workspace.to_json())

# convert the object into a dict
workspace_dict = workspace_instance.to_dict()
# create an instance of Workspace from a dict
workspace_from_dict = Workspace.from_dict(workspace_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


