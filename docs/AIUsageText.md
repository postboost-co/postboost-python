# AIUsageText


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**used** | **int** | &#x60;null&#x60; when the workspace has no text credit limit. | 
**limit** | **int** |  | 
**remaining** | **int** |  | 
**cycle_started_at** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.ai_usage_text import AIUsageText

# TODO update the JSON string below
json = "{}"
# create an instance of AIUsageText from a JSON string
ai_usage_text_instance = AIUsageText.from_json(json)
# print the JSON string representation of the object
print(AIUsageText.to_json())

# convert the object into a dict
ai_usage_text_dict = ai_usage_text_instance.to_dict()
# create an instance of AIUsageText from a dict
ai_usage_text_from_dict = AIUsageText.from_dict(ai_usage_text_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


