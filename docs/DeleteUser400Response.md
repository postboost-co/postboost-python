# DeleteUser400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from postboost.models.delete_user400_response import DeleteUser400Response

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteUser400Response from a JSON string
delete_user400_response_instance = DeleteUser400Response.from_json(json)
# print the JSON string representation of the object
print(DeleteUser400Response.to_json())

# convert the object into a dict
delete_user400_response_dict = delete_user400_response_instance.to_dict()
# create an instance of DeleteUser400Response from a dict
delete_user400_response_from_dict = DeleteUser400Response.from_dict(delete_user400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


