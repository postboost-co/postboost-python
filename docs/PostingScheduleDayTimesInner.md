# PostingScheduleDayTimesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **str** | Clock time &#x60;HH:MM&#x60; in the schedule&#39;s timezone. | 

## Example

```python
from postboost.models.posting_schedule_day_times_inner import PostingScheduleDayTimesInner

# TODO update the JSON string below
json = "{}"
# create an instance of PostingScheduleDayTimesInner from a JSON string
posting_schedule_day_times_inner_instance = PostingScheduleDayTimesInner.from_json(json)
# print the JSON string representation of the object
print(PostingScheduleDayTimesInner.to_json())

# convert the object into a dict
posting_schedule_day_times_inner_dict = posting_schedule_day_times_inner_instance.to_dict()
# create an instance of PostingScheduleDayTimesInner from a dict
posting_schedule_day_times_inner_from_dict = PostingScheduleDayTimesInner.from_dict(posting_schedule_day_times_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


