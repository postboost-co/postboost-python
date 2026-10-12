# BrandVoiceInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**business_name** | **str** |  | [optional] 
**mission** | **str** |  | [optional] 
**industry** | **str** |  | [optional] 
**personality** | **str** | How the brand sounds. The first sentence also feeds image prompts. | [optional] 
**audience** | **List[str]** |  | [optional] 
**topics_preferred** | **List[str]** |  | [optional] 
**topics_avoided** | **List[str]** |  | [optional] 
**tone_formal** | **int** | 1 very casual, 3 neutral, 5 very formal. | [optional] 
**tone_playful** | **int** | 1 strictly serious, 3 neutral, 5 very playful. | [optional] 
**tone_technical** | **int** | 1 very simple, 3 neutral, 5 highly technical. | [optional] 
**emoji_style** | **str** |  | [optional] 
**hashtag_strategy** | **str** |  | [optional] 
**avoid_words** | **List[str]** |  | [optional] 
**preferred_cta** | **List[str]** |  | [optional] 
**example_posts** | **List[Optional[str]]** |  | [optional] 

## Example

```python
from postboost.models.brand_voice_input import BrandVoiceInput

# TODO update the JSON string below
json = "{}"
# create an instance of BrandVoiceInput from a JSON string
brand_voice_input_instance = BrandVoiceInput.from_json(json)
# print the JSON string representation of the object
print(BrandVoiceInput.to_json())

# convert the object into a dict
brand_voice_input_dict = brand_voice_input_instance.to_dict()
# create an instance of BrandVoiceInput from a dict
brand_voice_input_from_dict = BrandVoiceInput.from_dict(brand_voice_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


