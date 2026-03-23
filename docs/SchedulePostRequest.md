# SchedulePostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_now** | **bool** |  | 

## Example

```python
from postboost.models.schedule_post_request import SchedulePostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SchedulePostRequest from a JSON string
schedule_post_request_instance = SchedulePostRequest.from_json(json)
# print the JSON string representation of the object
print(SchedulePostRequest.to_json())

# convert the object into a dict
schedule_post_request_dict = schedule_post_request_instance.to_dict()
# create an instance of SchedulePostRequest from a dict
schedule_post_request_from_dict = SchedulePostRequest.from_dict(schedule_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


