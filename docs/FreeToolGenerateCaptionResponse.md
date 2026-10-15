# FreeToolGenerateCaptionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**captions** | **List[str]** | Three different captions, each within the network&#39;s text limit (at most 2,200 characters). | [optional] 
**credits_spent** | **int** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] 
**cached** | **bool** | True when the same request was answered before (free). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_caption_response import FreeToolGenerateCaptionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateCaptionResponse from a JSON string
free_tool_generate_caption_response_instance = FreeToolGenerateCaptionResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateCaptionResponse.to_json())

# convert the object into a dict
free_tool_generate_caption_response_dict = free_tool_generate_caption_response_instance.to_dict()
# create an instance of FreeToolGenerateCaptionResponse from a dict
free_tool_generate_caption_response_from_dict = FreeToolGenerateCaptionResponse.from_dict(free_tool_generate_caption_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


