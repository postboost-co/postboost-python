# ScheduleResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**scheduled_at** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.schedule_result import ScheduleResult

# TODO update the JSON string below
json = "{}"
# create an instance of ScheduleResult from a JSON string
schedule_result_instance = ScheduleResult.from_json(json)
# print the JSON string representation of the object
print(ScheduleResult.to_json())

# convert the object into a dict
schedule_result_dict = schedule_result_instance.to_dict()
# create an instance of ScheduleResult from a dict
schedule_result_from_dict = ScheduleResult.from_dict(schedule_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


