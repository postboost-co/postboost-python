# DeletePostsBulkRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**posts** | **List[str]** | Array of post UUIDs to delete. | 
**trash** | **bool** | Move to trash instead of permanent delete. | [optional] [default to False]
**delete_mode** | [**DeleteMode**](DeleteMode.md) |  | [optional] [default to DeleteMode.APP_ONLY]

## Example

```python
from postboost.models.delete_posts_bulk_request import DeletePostsBulkRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeletePostsBulkRequest from a JSON string
delete_posts_bulk_request_instance = DeletePostsBulkRequest.from_json(json)
# print the JSON string representation of the object
print(DeletePostsBulkRequest.to_json())

# convert the object into a dict
delete_posts_bulk_request_dict = delete_posts_bulk_request_instance.to_dict()
# create an instance of DeletePostsBulkRequest from a dict
delete_posts_bulk_request_from_dict = DeletePostsBulkRequest.from_dict(delete_posts_bulk_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


