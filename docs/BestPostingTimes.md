# BestPostingTimes


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timezone** | **str** |  | 
**times** | [**List[BestPostingTimesTimesInner]**](BestPostingTimesTimesInner.md) | The next recommended time per account. Accounts without enough history are left out. | 

## Example

```python
from postboost.models.best_posting_times import BestPostingTimes

# TODO update the JSON string below
json = "{}"
# create an instance of BestPostingTimes from a JSON string
best_posting_times_instance = BestPostingTimes.from_json(json)
# print the JSON string representation of the object
print(BestPostingTimes.to_json())

# convert the object into a dict
best_posting_times_dict = best_posting_times_instance.to_dict()
# create an instance of BestPostingTimes from a dict
best_posting_times_from_dict = BestPostingTimes.from_dict(best_posting_times_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


