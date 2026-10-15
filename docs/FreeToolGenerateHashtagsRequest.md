# FreeToolGenerateHashtagsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**topic** | **str** | What the post is about. | 
**niche** | **str** | Optional niche from the hashtag generator page. | [optional] 
**network** | **str** | The network the text is written for. | [optional] [default to 'instagram']
**workspace** | **str** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_hashtags_request import FreeToolGenerateHashtagsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateHashtagsRequest from a JSON string
free_tool_generate_hashtags_request_instance = FreeToolGenerateHashtagsRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateHashtagsRequest.to_json())

# convert the object into a dict
free_tool_generate_hashtags_request_dict = free_tool_generate_hashtags_request_instance.to_dict()
# create an instance of FreeToolGenerateHashtagsRequest from a dict
free_tool_generate_hashtags_request_from_dict = FreeToolGenerateHashtagsRequest.from_dict(free_tool_generate_hashtags_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


