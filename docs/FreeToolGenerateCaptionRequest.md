# FreeToolGenerateCaptionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | What the post is about. | 
**tone** | **str** |  | [optional] [default to 'friendly']
**length** | **str** | short: 10-20 words, medium: 25-40, long: 45-60. | [optional] [default to 'medium']
**emoji** | **bool** | Use a few fitting emoji. | [optional] [default to True]
**hashtags** | **bool** | End each caption with 3-5 relevant hashtags. | [optional] [default to False]
**network** | **str** | The network the text is written for. | [optional] [default to 'instagram']
**workspace** | **str** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] 
**format** | **str** | caption: short captions (default). post: long-form posts of 300-600, 600-1,300 or 1,300-2,000 characters by &#x60;length&#x60;, with at most 3 hashtags; network linkedin only. | [optional] [default to 'caption']

## Example

```python
from postboost.models.free_tool_generate_caption_request import FreeToolGenerateCaptionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateCaptionRequest from a JSON string
free_tool_generate_caption_request_instance = FreeToolGenerateCaptionRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateCaptionRequest.to_json())

# convert the object into a dict
free_tool_generate_caption_request_dict = free_tool_generate_caption_request_instance.to_dict()
# create an instance of FreeToolGenerateCaptionRequest from a dict
free_tool_generate_caption_request_from_dict = FreeToolGenerateCaptionRequest.from_dict(free_tool_generate_caption_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


