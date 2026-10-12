# LearnBrandVoiceResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**BrandVoice**](BrandVoice.md) |  | 
**meta** | [**LearnBrandVoiceResponseMeta**](LearnBrandVoiceResponseMeta.md) |  | 

## Example

```python
from postboost.models.learn_brand_voice_response import LearnBrandVoiceResponse

# TODO update the JSON string below
json = "{}"
# create an instance of LearnBrandVoiceResponse from a JSON string
learn_brand_voice_response_instance = LearnBrandVoiceResponse.from_json(json)
# print the JSON string representation of the object
print(LearnBrandVoiceResponse.to_json())

# convert the object into a dict
learn_brand_voice_response_dict = learn_brand_voice_response_instance.to_dict()
# create an instance of LearnBrandVoiceResponse from a dict
learn_brand_voice_response_from_dict = LearnBrandVoiceResponse.from_dict(learn_brand_voice_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


