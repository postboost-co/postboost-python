# PostingScheduleDay


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Weekday, 1 (Monday) to 6 (Saturday), 0 (Sunday). | 
**status** | **bool** | Whether the queue posts on this day. | 
**times** | [**List[PostingScheduleDayTimesInner]**](PostingScheduleDayTimesInner.md) |  | 

## Example

```python
from postboost.models.posting_schedule_day import PostingScheduleDay

# TODO update the JSON string below
json = "{}"
# create an instance of PostingScheduleDay from a JSON string
posting_schedule_day_instance = PostingScheduleDay.from_json(json)
# print the JSON string representation of the object
print(PostingScheduleDay.to_json())

# convert the object into a dict
posting_schedule_day_dict = posting_schedule_day_instance.to_dict()
# create an instance of PostingScheduleDay from a dict
posting_schedule_day_from_dict = PostingScheduleDay.from_dict(posting_schedule_day_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


