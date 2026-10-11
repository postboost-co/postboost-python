# PostingTimeSlot


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**score** | **int** |  | 
**samples** | **int** |  | 
**confidence** | **str** |  | 

## Example

```python
from postboost.models.posting_time_slot import PostingTimeSlot

# TODO update the JSON string below
json = "{}"
# create an instance of PostingTimeSlot from a JSON string
posting_time_slot_instance = PostingTimeSlot.from_json(json)
# print the JSON string representation of the object
print(PostingTimeSlot.to_json())

# convert the object into a dict
posting_time_slot_dict = posting_time_slot_instance.to_dict()
# create an instance of PostingTimeSlot from a dict
posting_time_slot_from_dict = PostingTimeSlot.from_dict(posting_time_slot_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


