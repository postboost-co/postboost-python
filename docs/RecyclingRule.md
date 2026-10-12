# RecyclingRule


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | 
**type** | **str** |  | 
**post_uuid** | **str** |  | 
**tag_uuid** | **str** |  | 
**account_ids** | **List[int]** |  | 
**interval_days** | **int** |  | 
**max_runs** | **int** |  | 
**runs_done** | **int** | Copies created so far. | 
**placement** | **str** |  | 
**active** | **bool** |  | 
**next_run_at** | **datetime** |  | 
**last_run_at** | **datetime** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from postboost.models.recycling_rule import RecyclingRule

# TODO update the JSON string below
json = "{}"
# create an instance of RecyclingRule from a JSON string
recycling_rule_instance = RecyclingRule.from_json(json)
# print the JSON string representation of the object
print(RecyclingRule.to_json())

# convert the object into a dict
recycling_rule_dict = recycling_rule_instance.to_dict()
# create an instance of RecyclingRule from a dict
recycling_rule_from_dict = RecyclingRule.from_dict(recycling_rule_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


