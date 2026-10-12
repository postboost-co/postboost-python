# LearnBrandVoiceInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | **int** | How many of the latest published posts to read. | [optional] [default to 10]
**account_ids** | **List[int]** | Only read posts whose accounts are all among these. | [optional] 
**apply** | **bool** | Save the proposed voice as the workspace brand voice. | [optional] [default to False]
**overwrite** | **bool** | Let learned values replace fields that are already set. | [optional] [default to False]

## Example

```python
from postboost.models.learn_brand_voice_input import LearnBrandVoiceInput

# TODO update the JSON string below
json = "{}"
# create an instance of LearnBrandVoiceInput from a JSON string
learn_brand_voice_input_instance = LearnBrandVoiceInput.from_json(json)
# print the JSON string representation of the object
print(LearnBrandVoiceInput.to_json())

# convert the object into a dict
learn_brand_voice_input_dict = learn_brand_voice_input_instance.to_dict()
# create an instance of LearnBrandVoiceInput from a dict
learn_brand_voice_input_from_dict = LearnBrandVoiceInput.from_dict(learn_brand_voice_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


