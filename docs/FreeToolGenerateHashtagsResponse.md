# FreeToolGenerateHashtagsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hashtags** | **List[str]** | 5 to 10 hashtags (3 to 6 with network tiktok), best first. | [optional] 
**credits_spent** | **int** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] 
**cached** | **bool** | True when the same request was answered before (free). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_hashtags_response import FreeToolGenerateHashtagsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateHashtagsResponse from a JSON string
free_tool_generate_hashtags_response_instance = FreeToolGenerateHashtagsResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateHashtagsResponse.to_json())

# convert the object into a dict
free_tool_generate_hashtags_response_dict = free_tool_generate_hashtags_response_instance.to_dict()
# create an instance of FreeToolGenerateHashtagsResponse from a dict
free_tool_generate_hashtags_response_from_dict = FreeToolGenerateHashtagsResponse.from_dict(free_tool_generate_hashtags_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


