# AICredits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**available** | **bool** | Whether the workspace can spend AI credits now. Always true when no balance is tracked. | 
**balance** | **float** | Remaining credit balance (2 decimals), or null when no balance is tracked. | 
**low** | **bool** | True when the balance is above 0 and at most 10. | 

## Example

```python
from postboost.models.ai_credits import AICredits

# TODO update the JSON string below
json = "{}"
# create an instance of AICredits from a JSON string
ai_credits_instance = AICredits.from_json(json)
# print the JSON string representation of the object
print(AICredits.to_json())

# convert the object into a dict
ai_credits_dict = ai_credits_instance.to_dict()
# create an instance of AICredits from a dict
ai_credits_from_dict = AICredits.from_dict(ai_credits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


