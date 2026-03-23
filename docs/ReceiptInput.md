# ReceiptInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**workspace_uuid** | **str** |  | 
**transaction_id** | **str** |  | 
**invoice_number** | **str** |  | 
**amount** | **float** |  | 
**tax** | **float** |  | 
**currency** | **str** |  | 
**description** | **str** |  | [optional] 
**receipt_url** | **str** |  | [optional] 
**paid_at** | **date** |  | 

## Example

```python
from postboost.models.receipt_input import ReceiptInput

# TODO update the JSON string below
json = "{}"
# create an instance of ReceiptInput from a JSON string
receipt_input_instance = ReceiptInput.from_json(json)
# print the JSON string representation of the object
print(ReceiptInput.to_json())

# convert the object into a dict
receipt_input_dict = receipt_input_instance.to_dict()
# create an instance of ReceiptInput from a dict
receipt_input_from_dict = ReceiptInput.from_dict(receipt_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


