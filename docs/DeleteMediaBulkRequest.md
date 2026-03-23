# DeleteMediaBulkRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | **List[int]** | Array of media IDs to delete. | 

## Example

```python
from postboost.models.delete_media_bulk_request import DeleteMediaBulkRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteMediaBulkRequest from a JSON string
delete_media_bulk_request_instance = DeleteMediaBulkRequest.from_json(json)
# print the JSON string representation of the object
print(DeleteMediaBulkRequest.to_json())

# convert the object into a dict
delete_media_bulk_request_dict = delete_media_bulk_request_instance.to_dict()
# create an instance of DeleteMediaBulkRequest from a dict
delete_media_bulk_request_from_dict = DeleteMediaBulkRequest.from_dict(delete_media_bulk_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


