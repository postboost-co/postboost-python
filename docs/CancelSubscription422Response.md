# CancelSubscription422Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**errors** | [**CancelSubscription422ResponseErrors**](CancelSubscription422ResponseErrors.md) |  | [optional] 

## Example

```python
from postboost.models.cancel_subscription422_response import CancelSubscription422Response

# TODO update the JSON string below
json = "{}"
# create an instance of CancelSubscription422Response from a JSON string
cancel_subscription422_response_instance = CancelSubscription422Response.from_json(json)
# print the JSON string representation of the object
print(CancelSubscription422Response.to_json())

# convert the object into a dict
cancel_subscription422_response_dict = cancel_subscription422_response_instance.to_dict()
# create an instance of CancelSubscription422Response from a dict
cancel_subscription422_response_from_dict = CancelSubscription422Response.from_dict(cancel_subscription422_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


