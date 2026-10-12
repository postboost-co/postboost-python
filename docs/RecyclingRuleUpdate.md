# RecyclingRuleUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**interval_days** | **int** |  | [optional] 
**max_runs** | **int** |  | [optional] 
**placement** | **str** |  | [optional] 
**account_ids** | **List[int]** |  | [optional] 
**start_at** | **datetime** | Next run. | [optional] 
**active** | **bool** |  | [optional] 

## Example

```python
from postboost.models.recycling_rule_update import RecyclingRuleUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of RecyclingRuleUpdate from a JSON string
recycling_rule_update_instance = RecyclingRuleUpdate.from_json(json)
# print the JSON string representation of the object
print(RecyclingRuleUpdate.to_json())

# convert the object into a dict
recycling_rule_update_dict = recycling_rule_update_instance.to_dict()
# create an instance of RecyclingRuleUpdate from a dict
recycling_rule_update_from_dict = RecyclingRuleUpdate.from_dict(recycling_rule_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


