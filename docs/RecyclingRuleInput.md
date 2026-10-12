# RecyclingRuleInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**interval_days** | **int** | Days between copies. | 
**max_runs** | **int** | Copies to create before the rule stops; null &#x3D; no limit. | [optional] 
**placement** | **str** | &#x60;queue&#x60;: each account&#39;s next free queue slot (skipped when the queue is full for 14 days). &#x60;same_time&#x60;: the source post&#39;s time of day. &#x60;draft&#x60;: a draft only. | [optional] [default to 'queue']
**account_ids** | **List[int]** | Accounts for the copies; default the source post&#39;s accounts. For a tag pool, limits each picked post&#39;s accounts. | [optional] 
**start_at** | **datetime** | First run; default one interval from now. | [optional] 
**active** | **bool** |  | [optional] [default to True]
**type** | **str** | Defaults to &#x60;post&#x60; when &#x60;post_uuid&#x60; is sent, else &#x60;tag_pool&#x60;. | [optional] 
**post_uuid** | **str** | The post to recycle (type &#x60;post&#x60;). | [optional] 
**tag_uuid** | **str** | The tag whose published posts are recycled, least recently recycled first (type &#x60;tag_pool&#x60;). | [optional] 

## Example

```python
from postboost.models.recycling_rule_input import RecyclingRuleInput

# TODO update the JSON string below
json = "{}"
# create an instance of RecyclingRuleInput from a JSON string
recycling_rule_input_instance = RecyclingRuleInput.from_json(json)
# print the JSON string representation of the object
print(RecyclingRuleInput.to_json())

# convert the object into a dict
recycling_rule_input_dict = recycling_rule_input_instance.to_dict()
# create an instance of RecyclingRuleInput from a dict
recycling_rule_input_from_dict = RecyclingRuleInput.from_dict(recycling_rule_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


