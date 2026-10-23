# FreeToolGenerateBrandVoiceResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**voice** | [**FreeToolGenerateBrandVoiceResponseVoice**](FreeToolGenerateBrandVoiceResponseVoice.md) |  | [optional] 
**evidence** | **Dict[str, List[str]]** | Per trait key, up to 2 quotes from your posts that show it; only quotes found in your posts are kept, so a list can be empty. | [optional] 
**system_prompt** | **str** | The system prompt PostBoost&#39;s AI uses for this voice; paste it into ChatGPT, Claude or your agent. | [optional] 
**markdown** | **str** | The voice as a Markdown guide with its quotes, ending with the system prompt. | [optional] 
**credits_spent** | **int** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] 
**cached** | **bool** | True when the same request was answered before (free). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_brand_voice_response import FreeToolGenerateBrandVoiceResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateBrandVoiceResponse from a JSON string
free_tool_generate_brand_voice_response_instance = FreeToolGenerateBrandVoiceResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateBrandVoiceResponse.to_json())

# convert the object into a dict
free_tool_generate_brand_voice_response_dict = free_tool_generate_brand_voice_response_instance.to_dict()
# create an instance of FreeToolGenerateBrandVoiceResponse from a dict
free_tool_generate_brand_voice_response_from_dict = FreeToolGenerateBrandVoiceResponse.from_dict(free_tool_generate_brand_voice_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


