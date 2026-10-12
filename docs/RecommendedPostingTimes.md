# RecommendedPostingTimes


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**has_data** | **bool** |  | 
**timezone** | **str** |  | [optional] 
**slots_per_day** | **int** |  | 
**samples** | **int** | Number of past posts the recommendation is based on. | 
**times** | **List[Dict[str, object]]** | Recommended times per weekday. | 

## Example

```python
from postboost.models.recommended_posting_times import RecommendedPostingTimes

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendedPostingTimes from a JSON string
recommended_posting_times_instance = RecommendedPostingTimes.from_json(json)
# print the JSON string representation of the object
print(RecommendedPostingTimes.to_json())

# convert the object into a dict
recommended_posting_times_dict = recommended_posting_times_instance.to_dict()
# create an instance of RecommendedPostingTimes from a dict
recommended_posting_times_from_dict = RecommendedPostingTimes.from_dict(recommended_posting_times_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


