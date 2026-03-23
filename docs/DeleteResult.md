# DeleteResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deleted** | **bool** |  | 
**deleted_from_app** | **bool** |  | 
**to_trash** | **bool** |  | 

## Example

```python
from postboost.models.delete_result import DeleteResult

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteResult from a JSON string
delete_result_instance = DeleteResult.from_json(json)
# print the JSON string representation of the object
print(DeleteResult.to_json())

# convert the object into a dict
delete_result_dict = delete_result_instance.to_dict()
# create an instance of DeleteResult from a dict
delete_result_from_dict = DeleteResult.from_dict(delete_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


