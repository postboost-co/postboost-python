# SubscriptionInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_subscription_id** | **str** |  | 
**platform_plan_id** | **str** |  | 
**status** | [**SubscriptionStatus**](SubscriptionStatus.md) |  | 
**trial_ends_at** | **datetime** | Required when status is &#x60;trialing&#x60;. | [optional] 

## Example

```python
from postboost.models.subscription_input import SubscriptionInput

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionInput from a JSON string
subscription_input_instance = SubscriptionInput.from_json(json)
# print the JSON string representation of the object
print(SubscriptionInput.to_json())

# convert the object into a dict
subscription_input_dict = subscription_input_instance.to_dict()
# create an instance of SubscriptionInput from a dict
subscription_input_from_dict = SubscriptionInput.from_dict(subscription_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


