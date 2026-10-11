# ApprovePostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** | New date for the post (Y-m-d). Use together with &#x60;time&#x60;. | [optional] 
**time** | **str** | New time for the post (H:i). | [optional] 
**timezone** | **str** | Timezone &#x60;date&#x60;, &#x60;time&#x60; and &#x60;accounts_schedule&#x60; are read in. Defaults to the workspace timezone. | [optional] 
**accounts_schedule** | [**List[AccountSchedule]**](AccountSchedule.md) | Per-account departure times. When omitted, accounts keep their offsets from the post time. | [optional] 

## Example

```python
from postboost.models.approve_post_request import ApprovePostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ApprovePostRequest from a JSON string
approve_post_request_instance = ApprovePostRequest.from_json(json)
# print the JSON string representation of the object
print(ApprovePostRequest.to_json())

# convert the object into a dict
approve_post_request_dict = approve_post_request_instance.to_dict()
# create an instance of ApprovePostRequest from a dict
approve_post_request_from_dict = ApprovePostRequest.from_dict(approve_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


