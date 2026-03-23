# SubscriptionUpdateInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_plan_id** | **str** |  | 
**status** | [**SubscriptionStatus**](SubscriptionStatus.md) |  | 
**trial_ends_at** | **datetime** | Required when status is &#x60;trialing&#x60;. | [optional] 
**paused_from** | **datetime** | Required when status is &#x60;paused&#x60;. | [optional] 

## Example

```python
from postboost.models.subscription_update_input import SubscriptionUpdateInput

# TODO update the JSON string below
json = "{}"
# create an instance of SubscriptionUpdateInput from a JSON string
subscription_update_input_instance = SubscriptionUpdateInput.from_json(json)
# print the JSON string representation of the object
print(SubscriptionUpdateInput.to_json())

# convert the object into a dict
subscription_update_input_dict = subscription_update_input_instance.to_dict()
# create an instance of SubscriptionUpdateInput from a dict
subscription_update_input_from_dict = SubscriptionUpdateInput.from_dict(subscription_update_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


