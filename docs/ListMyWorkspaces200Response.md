# ListMyWorkspaces200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[PublicWorkspace]**](PublicWorkspace.md) |  | [optional] 

## Example

```python
from postboost.models.list_my_workspaces200_response import ListMyWorkspaces200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListMyWorkspaces200Response from a JSON string
list_my_workspaces200_response_instance = ListMyWorkspaces200Response.from_json(json)
# print the JSON string representation of the object
print(ListMyWorkspaces200Response.to_json())

# convert the object into a dict
list_my_workspaces200_response_dict = list_my_workspaces200_response_instance.to_dict()
# create an instance of ListMyWorkspaces200Response from a dict
list_my_workspaces200_response_from_dict = ListMyWorkspaces200Response.from_dict(list_my_workspaces200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


