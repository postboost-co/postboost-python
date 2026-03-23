# ReceiptUpdateInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**transaction_id** | **str** |  | 
**invoice_number** | **str** |  | 
**amount** | **float** |  | 
**tax** | **float** |  | [optional] 
**currency** | **str** |  | 
**description** | **str** |  | [optional] 
**receipt_url** | **str** |  | [optional] 
**paid_at** | **date** |  | 

## Example

```python
from postboost.models.receipt_update_input import ReceiptUpdateInput

# TODO update the JSON string below
json = "{}"
# create an instance of ReceiptUpdateInput from a JSON string
receipt_update_input_instance = ReceiptUpdateInput.from_json(json)
# print the JSON string representation of the object
print(ReceiptUpdateInput.to_json())

# convert the object into a dict
receipt_update_input_dict = receipt_update_input_instance.to_dict()
# create an instance of ReceiptUpdateInput from a dict
receipt_update_input_from_dict = ReceiptUpdateInput.from_dict(receipt_update_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


