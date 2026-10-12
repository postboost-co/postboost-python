# RecyclingRuleSettings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**interval_days** | **int** | Days between copies. | 
**max_runs** | **int** | Copies to create before the rule stops; null &#x3D; no limit. | [optional] 
**placement** | **str** | &#x60;queue&#x60;: each account&#39;s next free queue slot (skipped when the queue is full for 14 days). &#x60;same_time&#x60;: the source post&#39;s time of day. &#x60;draft&#x60;: a draft only. | [optional] [default to 'queue']
**account_ids** | **List[int]** | Accounts for the copies; default the source post&#39;s accounts. For a tag pool, limits each picked post&#39;s accounts. | [optional] 
**start_at** | **datetime** | First run; default one interval from now. | [optional] 
**active** | **bool** |  | [optional] [default to True]

## Example

```python
from postboost.models.recycling_rule_settings import RecyclingRuleSettings

# TODO update the JSON string below
json = "{}"
# create an instance of RecyclingRuleSettings from a JSON string
recycling_rule_settings_instance = RecyclingRuleSettings.from_json(json)
# print the JSON string representation of the object
print(RecyclingRuleSettings.to_json())

# convert the object into a dict
recycling_rule_settings_dict = recycling_rule_settings_instance.to_dict()
# create an instance of RecyclingRuleSettings from a dict
recycling_rule_settings_from_dict = RecyclingRuleSettings.from_dict(recycling_rule_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


