# Receipt


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | 
**transaction_id** | **str** |  | 
**invoice_number** | **str** |  | 
**amount** | **float** |  | 
**tax** | **float** |  | 
**currency** | **str** |  | 
**receipt_url** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**paid_at** | **str** | Display date in the configured timezone, &#x60;M j, Y&#x60; (not RFC 3339). | 
**created_at** | **str** | Display date in the configured timezone, &#x60;M j, Y&#x60; (not RFC 3339). | 

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


