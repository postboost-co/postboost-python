# CheckoutSubscriptionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan_id** | **int** |  | 
**cycle** | **str** |  | 
**coupon** | **str** |  | [optional] 

## Example

```python
from postboost.models.checkout_subscription_request import CheckoutSubscriptionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CheckoutSubscriptionRequest from a JSON string
checkout_subscription_request_instance = CheckoutSubscriptionRequest.from_json(json)
# print the JSON string representation of the object
print(CheckoutSubscriptionRequest.to_json())

# convert the object into a dict
checkout_subscription_request_dict = checkout_subscription_request_instance.to_dict()
# create an instance of CheckoutSubscriptionRequest from a dict
checkout_subscription_request_from_dict = CheckoutSubscriptionRequest.from_dict(checkout_subscription_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


