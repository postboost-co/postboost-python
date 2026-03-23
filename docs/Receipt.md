# Receipt


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | [optional] 
**transaction_id** | **str** |  | [optional] 
**invoice_number** | **str** |  | [optional] 
**amount** | **float** |  | [optional] 
**tax** | **float** |  | [optional] 
**currency** | **str** |  | [optional] 
**receipt_url** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**paid_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.receipt import Receipt

# TODO update the JSON string below
json = "{}"
# create an instance of Receipt from a JSON string
receipt_instance = Receipt.from_json(json)
# print the JSON string representation of the object
print(Receipt.to_json())

# convert the object into a dict
receipt_dict = receipt_instance.to_dict()
# create an instance of Receipt from a dict
receipt_from_dict = Receipt.from_dict(receipt_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


