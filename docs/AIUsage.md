# AIUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | [**AIUsageText**](AIUsageText.md) |  | 
**image** | [**ImageCreditBalance**](ImageCreditBalance.md) |  | 

## Example

```python
from postboost.models.ai_usage import AIUsage

# TODO update the JSON string below
json = "{}"
# create an instance of AIUsage from a JSON string
ai_usage_instance = AIUsage.from_json(json)
# print the JSON string representation of the object
print(AIUsage.to_json())

# convert the object into a dict
ai_usage_dict = ai_usage_instance.to_dict()
# create an instance of AIUsage from a dict
ai_usage_from_dict = AIUsage.from_dict(ai_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


