# BrandVoice


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**business_name** | **str** |  | [optional] 
**mission** | **str** |  | [optional] 
**industry** | **str** |  | [optional] 
**personality** | **str** |  | [optional] 
**audience** | **List[str]** |  | [optional] 
**topics_preferred** | **List[str]** |  | [optional] 
**topics_avoided** | **List[str]** |  | [optional] 
**tone_formal** | **int** |  | 
**tone_playful** | **int** |  | 
**tone_technical** | **int** |  | 
**emoji_style** | **str** |  | 
**hashtag_strategy** | **str** |  | 
**avoid_words** | **List[str]** |  | [optional] 
**preferred_cta** | **List[str]** |  | [optional] 
**example_posts** | **List[Optional[str]]** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.brand_voice import BrandVoice

# TODO update the JSON string below
json = "{}"
# create an instance of BrandVoice from a JSON string
brand_voice_instance = BrandVoice.from_json(json)
# print the JSON string representation of the object
print(BrandVoice.to_json())

# convert the object into a dict
brand_voice_dict = brand_voice_instance.to_dict()
# create an instance of BrandVoice from a dict
brand_voice_from_dict = BrandVoice.from_dict(brand_voice_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


