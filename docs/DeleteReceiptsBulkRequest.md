# DeleteReceiptsBulkRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**receipts** | **List[str]** |  | 

## Example

```python
from postboost.models.delete_receipts_bulk_request import DeleteReceiptsBulkRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteReceiptsBulkRequest from a JSON string
delete_receipts_bulk_request_instance = DeleteReceiptsBulkRequest.from_json(json)
# print the JSON string representation of the object
print(DeleteReceiptsBulkRequest.to_json())

# convert the object into a dict
delete_receipts_bulk_request_dict = delete_receipts_bulk_request_instance.to_dict()
# create an instance of DeleteReceiptsBulkRequest from a dict
delete_receipts_bulk_request_from_dict = DeleteReceiptsBulkRequest.from_dict(delete_receipts_bulk_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


