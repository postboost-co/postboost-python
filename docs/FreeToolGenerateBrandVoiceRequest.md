# FreeToolGenerateBrandVoiceRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**posts** | **List[str]** | Your own posts, one per item: 3 to 10 different posts of 20 to 3,200 characters, 20,000 in total. An exact copy counts once. | 
**business_name** | **str** | Your business name, used as given (never generated). | [optional] 
**industry** | **str** | Your industry, used as given (never generated). | [optional] 
**workspace** | **str** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_brand_voice_request import FreeToolGenerateBrandVoiceRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateBrandVoiceRequest from a JSON string
free_tool_generate_brand_voice_request_instance = FreeToolGenerateBrandVoiceRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateBrandVoiceRequest.to_json())

# convert the object into a dict
free_tool_generate_brand_voice_request_dict = free_tool_generate_brand_voice_request_instance.to_dict()
# create an instance of FreeToolGenerateBrandVoiceRequest from a dict
free_tool_generate_brand_voice_request_from_dict = FreeToolGenerateBrandVoiceRequest.from_dict(free_tool_generate_brand_voice_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


