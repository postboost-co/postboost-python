# PostingScheduleInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **int** | 0 for the workspace schedule, or an account &#x60;id&#x60;. | 
**timezone** | **str** |  | 
**auto_tune** | **bool** |  | [optional] 
**times** | [**List[PostingScheduleDay]**](PostingScheduleDay.md) |  | 

## Example

```python
from postboost.models.posting_schedule_input import PostingScheduleInput

# TODO update the JSON string below
json = "{}"
# create an instance of PostingScheduleInput from a JSON string
posting_schedule_input_instance = PostingScheduleInput.from_json(json)
# print the JSON string representation of the object
print(PostingScheduleInput.to_json())

# convert the object into a dict
posting_schedule_input_dict = posting_schedule_input_instance.to_dict()
# create an instance of PostingScheduleInput from a dict
posting_schedule_input_from_dict = PostingScheduleInput.from_dict(posting_schedule_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


