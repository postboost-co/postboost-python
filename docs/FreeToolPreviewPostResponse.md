# FreeToolPreviewPostResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**networks** | [**List[FreeToolPreviewPostResponseNetworksInner]**](FreeToolPreviewPostResponseNetworksInner.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_preview_post_response import FreeToolPreviewPostResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPreviewPostResponse from a JSON string
free_tool_preview_post_response_instance = FreeToolPreviewPostResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolPreviewPostResponse.to_json())

# convert the object into a dict
free_tool_preview_post_response_dict = free_tool_preview_post_response_instance.to_dict()
# create an instance of FreeToolPreviewPostResponse from a dict
free_tool_preview_post_response_from_dict = FreeToolPreviewPostResponse.from_dict(free_tool_preview_post_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


