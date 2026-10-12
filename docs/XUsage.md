# XUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period_start** | **datetime** |  | 
**period_end** | **datetime** |  | 
**enforced** | **bool** | Whether an allowance applies to this workspace. | 
**posts** | [**XUsageCounter**](XUsageCounter.md) |  | 
**link_posts** | [**XUsageCounter**](XUsageCounter.md) |  | 
**estimated_cost_usd** | **float** | PostBoost&#39;s estimate of what X charged for these posts. Informational; you are not billed per post. | 

## Example

```python
from postboost.models.x_usage import XUsage

# TODO update the JSON string below
json = "{}"
# create an instance of XUsage from a JSON string
x_usage_instance = XUsage.from_json(json)
# print the JSON string representation of the object
print(XUsage.to_json())

# convert the object into a dict
x_usage_dict = x_usage_instance.to_dict()
# create an instance of XUsage from a dict
x_usage_from_dict = XUsage.from_dict(x_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


