# PostingTimesDaysInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**score** | **int** |  | 
**samples** | **int** |  | 
**confidence** | **str** |  | 
**day** | **int** |  | 

## Example

```python
from postboost.models.posting_times_days_inner import PostingTimesDaysInner

# TODO update the JSON string below
json = "{}"
# create an instance of PostingTimesDaysInner from a JSON string
posting_times_days_inner_instance = PostingTimesDaysInner.from_json(json)
# print the JSON string representation of the object
print(PostingTimesDaysInner.to_json())

# convert the object into a dict
posting_times_days_inner_dict = posting_times_days_inner_instance.to_dict()
# create an instance of PostingTimesDaysInner from a dict
posting_times_days_inner_from_dict = PostingTimesDaysInner.from_dict(posting_times_days_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


