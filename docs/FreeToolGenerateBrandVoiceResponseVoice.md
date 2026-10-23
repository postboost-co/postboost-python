# FreeToolGenerateBrandVoiceResponseVoice

The voice in PostBoost's brand voice format (the workspace brand voice fields).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**business_name** | **str** | Your input, or null. | [optional] 
**mission** | **str** | Only when the posts state it, else null. | [optional] 
**industry** | **str** | Your input, or null. | [optional] 
**personality** | **str** | How the brand sounds. | [optional] 
**audience** | **List[str]** | Who the posts speak to. At most 8 items. | [optional] 
**topics_preferred** | **List[str]** | Topics the posts come back to. At most 8 items. | [optional] 
**topics_avoided** | **List[str]** | Topics the posts clearly steer away from; often empty. At most 8 items. | [optional] 
**tone_formal** | **int** | 1 very casual to 5 very formal, 3 neutral. | [optional] 
**tone_playful** | **int** | 1 very serious to 5 very playful, 3 neutral. | [optional] 
**tone_technical** | **int** | 1 very simple to 5 very technical, 3 neutral. | [optional] 
**emoji_style** | **str** |  | [optional] 
**hashtag_strategy** | **str** |  | [optional] 
**avoid_words** | **List[str]** | Words the posts clearly avoid; often empty. At most 8 items. | [optional] 
**preferred_cta** | **List[str]** | Calls to action the posts use. At most 8 items. | [optional] 
**example_posts** | **List[str]** | Up to 5 of your posts that sound most typical, exactly as given. | [optional] 

## Example

```python
from postboost.models.free_tool_generate_brand_voice_response_voice import FreeToolGenerateBrandVoiceResponseVoice

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateBrandVoiceResponseVoice from a JSON string
free_tool_generate_brand_voice_response_voice_instance = FreeToolGenerateBrandVoiceResponseVoice.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateBrandVoiceResponseVoice.to_json())

# convert the object into a dict
free_tool_generate_brand_voice_response_voice_dict = free_tool_generate_brand_voice_response_voice_instance.to_dict()
# create an instance of FreeToolGenerateBrandVoiceResponseVoice from a dict
free_tool_generate_brand_voice_response_voice_from_dict = FreeToolGenerateBrandVoiceResponseVoice.from_dict(free_tool_generate_brand_voice_response_voice_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


