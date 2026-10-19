# FreeToolGenerateYoutubeTitlesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**titles** | **List[str]** | Three to five different titles, each at most 100 characters, with the main keyword early, no &#x60;&lt;&#x60; or &#x60;&gt;&#x60; and not in capitals. | [optional] 
**credits_spent** | **int** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] 
**cached** | **bool** | True when the same request was answered before (free). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_youtube_titles_response import FreeToolGenerateYoutubeTitlesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateYoutubeTitlesResponse from a JSON string
free_tool_generate_youtube_titles_response_instance = FreeToolGenerateYoutubeTitlesResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateYoutubeTitlesResponse.to_json())

# convert the object into a dict
free_tool_generate_youtube_titles_response_dict = free_tool_generate_youtube_titles_response_instance.to_dict()
# create an instance of FreeToolGenerateYoutubeTitlesResponse from a dict
free_tool_generate_youtube_titles_response_from_dict = FreeToolGenerateYoutubeTitlesResponse.from_dict(free_tool_generate_youtube_titles_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


