# PostingTimes


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**has_data** | **bool** |  | 
**timezone** | **str** |  | 
**offset_hours** | **int** |  | 
**accounts** | **int** | Accounts that contributed scores. | 
**samples** | **int** |  | 
**days** | [**List[PostingTimesDaysInner]**](PostingTimesDaysInner.md) | One entry per weekday (&#x60;day&#x60; 0 &#x3D; Sunday). | 
**day_intervals** | **List[List[PostingTimesDayIntervalsInnerInner]]** | Per weekday, 2-hour intervals. | 
**best** | [**List[PostingTimesBestInner]**](PostingTimesBestInner.md) | Up to three recommended slots, at most one per weekday. | 

## Example

```python
from postboost.models.posting_times import PostingTimes

# TODO update the JSON string below
json = "{}"
# create an instance of PostingTimes from a JSON string
posting_times_instance = PostingTimes.from_json(json)
# print the JSON string representation of the object
print(PostingTimes.to_json())

# convert the object into a dict
posting_times_dict = posting_times_instance.to_dict()
# create an instance of PostingTimes from a dict
posting_times_from_dict = PostingTimes.from_dict(posting_times_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


