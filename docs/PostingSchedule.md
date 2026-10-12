# PostingSchedule


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **int** | The account asked for; 0 for the workspace schedule. | 
**source_account_id** | **int** | Whose schedule applies; 0 when the workspace schedule applies. | 
**inherited** | **bool** | True when the account follows the workspace schedule. | 
**timezone** | **str** |  | 
**auto_tune** | **bool** | Adjust times automatically from engagement data. | 
**times** | [**List[PostingScheduleDay]**](PostingScheduleDay.md) |  | 

## Example

```python
from postboost.models.posting_schedule import PostingSchedule

# TODO update the JSON string below
json = "{}"
# create an instance of PostingSchedule from a JSON string
posting_schedule_instance = PostingSchedule.from_json(json)
# print the JSON string representation of the object
print(PostingSchedule.to_json())

# convert the object into a dict
posting_schedule_dict = posting_schedule_instance.to_dict()
# create an instance of PostingSchedule from a dict
posting_schedule_from_dict = PostingSchedule.from_dict(posting_schedule_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


