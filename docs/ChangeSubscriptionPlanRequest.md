# ChangeSubscriptionPlanRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**plan_id** | **int** |  | 
**cycle** | **str** |  | 
**prorate** | **bool** |  | 
**billing_immediately** | **bool** |  | 

## Example

```python
from postboost.models.change_subscription_plan_request import ChangeSubscriptionPlanRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ChangeSubscriptionPlanRequest from a JSON string
change_subscription_plan_request_instance = ChangeSubscriptionPlanRequest.from_json(json)
# print the JSON string representation of the object
print(ChangeSubscriptionPlanRequest.to_json())

# convert the object into a dict
change_subscription_plan_request_dict = change_subscription_plan_request_instance.to_dict()
# create an instance of ChangeSubscriptionPlanRequest from a dict
change_subscription_plan_request_from_dict = ChangeSubscriptionPlanRequest.from_dict(change_subscription_plan_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


