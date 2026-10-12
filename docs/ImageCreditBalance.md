# ImageCreditBalance


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | &#x60;false&#x60; when images are charged to text credits instead (the pool is switched off). | 
**used** | **int** |  | 
**limit** | **int** | Image credits this month; &#x60;null&#x60; &#x3D; no limit. | 
**remaining** | **int** |  | 
**period_start** | **datetime** |  | 
**period_end** | **datetime** |  | 

## Example

```python
from postboost.models.image_credit_balance import ImageCreditBalance

# TODO update the JSON string below
json = "{}"
# create an instance of ImageCreditBalance from a JSON string
image_credit_balance_instance = ImageCreditBalance.from_json(json)
# print the JSON string representation of the object
print(ImageCreditBalance.to_json())

# convert the object into a dict
image_credit_balance_dict = image_credit_balance_instance.to_dict()
# create an instance of ImageCreditBalance from a dict
image_credit_balance_from_dict = ImageCreditBalance.from_dict(image_credit_balance_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


