# PublicWorkspace


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**uuid** | **str** |  | 
**name** | **str** |  | 
**pivot** | [**PublicWorkspacePivot**](PublicWorkspacePivot.md) |  | [optional] 

## Example

```python
from postboost.models.public_workspace import PublicWorkspace

# TODO update the JSON string below
json = "{}"
# create an instance of PublicWorkspace from a JSON string
public_workspace_instance = PublicWorkspace.from_json(json)
# print the JSON string representation of the object
print(PublicWorkspace.to_json())

# convert the object into a dict
public_workspace_dict = public_workspace_instance.to_dict()
# create an instance of PublicWorkspace from a dict
public_workspace_from_dict = PublicWorkspace.from_dict(public_workspace_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


