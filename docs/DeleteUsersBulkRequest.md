# DeleteUsersBulkRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**users** | **List[int]** |  | 

## Example

```python
from postboost.models.delete_users_bulk_request import DeleteUsersBulkRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteUsersBulkRequest from a JSON string
delete_users_bulk_request_instance = DeleteUsersBulkRequest.from_json(json)
# print the JSON string representation of the object
print(DeleteUsersBulkRequest.to_json())

# convert the object into a dict
delete_users_bulk_request_dict = delete_users_bulk_request_instance.to_dict()
# create an instance of DeleteUsersBulkRequest from a dict
delete_users_bulk_request_from_dict = DeleteUsersBulkRequest.from_dict(delete_users_bulk_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


