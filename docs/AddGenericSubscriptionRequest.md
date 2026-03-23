# AddGenericSubscriptionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan_id** | **int** |  | 
**trial_days** | **int** |  | [optional] 
**keep_prev_trial_ends_at** | **bool** |  | 

## Example

```python
from postboost.models.add_generic_subscription_request import AddGenericSubscriptionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AddGenericSubscriptionRequest from a JSON string
add_generic_subscription_request_instance = AddGenericSubscriptionRequest.from_json(json)
# print the JSON string representation of the object
print(AddGenericSubscriptionRequest.to_json())

# convert the object into a dict
add_generic_subscription_request_dict = add_generic_subscription_request_instance.to_dict()
# create an instance of AddGenericSubscriptionRequest from a dict
add_generic_subscription_request_from_dict = AddGenericSubscriptionRequest.from_dict(add_generic_subscription_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


