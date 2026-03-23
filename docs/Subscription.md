# Subscription


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**platform_subscription_id** | **str** |  | 
**platform_plan_id** | **str** |  | 
**status** | [**SubscriptionStatus**](SubscriptionStatus.md) |  | 
**recurring** | **bool** |  | 
**trial_ends_at** | **datetime** |  | [optional] 
**paused_from** | **datetime** |  | [optional] 
**ends_at** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.subscription import Subscription

# TODO update the JSON string below
json = "{}"
# create an instance of Subscription from a JSON string
subscription_instance = Subscription.from_json(json)
# print the JSON string representation of the object
print(Subscription.to_json())

# convert the object into a dict
subscription_dict = subscription_instance.to_dict()
# create an instance of Subscription from a dict
subscription_from_dict = Subscription.from_dict(subscription_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


