# FreeToolPreviewPostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**instagram_ratio** | **str** | Image ratio of the Instagram feed post. | [optional] [default to '1:1']
**image_width** | **int** | Image width in pixels. Give it with image_height to get display_ratio and cropped per card. | [optional] 
**image_height** | **int** | Image height in pixels. Give it with image_width. | [optional] 

## Example

```python
from postboost.models.free_tool_preview_post_request import FreeToolPreviewPostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPreviewPostRequest from a JSON string
free_tool_preview_post_request_instance = FreeToolPreviewPostRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolPreviewPostRequest.to_json())

# convert the object into a dict
free_tool_preview_post_request_dict = free_tool_preview_post_request_instance.to_dict()
# create an instance of FreeToolPreviewPostRequest from a dict
free_tool_preview_post_request_from_dict = FreeToolPreviewPostRequest.from_dict(free_tool_preview_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


